# Progress Update: Week #9

Next Friday I'm pitching Galapag.us for ITP Pitch Fest to a venture-minded crowd.  Not my favorite thing in the world, because there's always a litany of responses that don't often make sense ("I want more detail", "I want less detail", "too much going on", "there should be one big button and that's it").  Everyone has their own preferences and there's too much emphasis placed on the precision of presentations -- personally I'm just happy if a presenter keeps the thing moving very very quickly and doesn't get flustered, try to get something working that's not going to work, etc.

Anyway what came out of our ITP Pitch Fest workshop on Friday was that I need to clone my thesis presentation deck and strip it down for a business mindset, and that'll help the final product.  I was also advised to come up with a use case for who would use Galapag.us and how it'd help him, as that'd be the best way to mitigate confusion.  So that's my priority for the upcoming week.

Also what came out of this is how tightening the screws at this stage of the thesis is getting interesting: if I need a use case, then I can create 5 random famous people, then assign them to tribes, and then show the audience how one can add a profile for someone else, then enter some data about them, and immediately get stock market-like charts of their metrics over time against their tribe and against country-level data.  And I can show how fluid and organic the whole process is.  I'm excited that, after so much time building the building blocks for the site, I can finally begin playing with the damn thing!

I also need to enable the next version of the site online.  I just have to clone my git repo after enabling some more routes, and then test to make sure the hosting environment is configured correctly.

Code-wise, I had some good breakthroughs; I found [Ilya Grigorik](http://www.igvita.com/), an engineer and dev advocate for Google, who's posted a ton on how to make web sites load faster.  I'm pretty happy to have restructured my code so that average response time falls within 400ms to under a second on a flat server.  The user experience is so much better.

Another breakthrough was getting equals, less than, greater than working with formulas, so now people can poll the database and create metrics based on equivalencies with user-provided values, i.e. I want to see if this person has a total number of x greater than 15.  As a result, I have a basic Galapag.us citizenship metric:

`individual_stats:total_prunings@gt@4 + individual_stats:profile_completion@gt@69 + individual_stats:membership_age@gt@3 + individual_stats:total_curations@gt@9 + individual_stats:total_referrals@gt@1`

I managed to figure out IP/API key throttling for anti-spam protection, and cleaned up my install scripts so that a fresh install will work just by running one python script.

I also talked to the CTO of a happiness-related tech company for a job interview.  I ended up doing a coding exercise in CoffeeScript and Backbone.js to interact with an API.  Backbone.js is a steep learning curve.  But we'll see if I might have a future with them.  They're doing positive psychology games to improve happiness.

And finally, I ordered a few test t-shirts, new business cards, and a Galápagos map for the ITP Spring Show.  They're going to look great!

This next week: meet with Heather on Monday, prepare the pitch for Friday, create a smooth use case pipeline, enable the site online.

Things slipping on the schedule: filling out API route coverage, admin panel controls for user abuse/management.

From github:

* font changes to IM Fell, made available offline too
* filled out tribe page w/ redis/mongo backend member keys, added offline javascript in case of loss of connection
* add tids to redis for tribes, tribe page started, decided not to make edit button (just delete, then add instead)
* global_stats now in redis, pageload speed improvements thx to Google PageSpeed, rate limiting for API/routes, remove category item button enabled, fork/edit for formulas are working
* added api key to models and profile settings page
* added highcharts & qr code to genome, heartbeat, settings
* wiring up formulas to formula pages, formula ratings
* some fixes to personality types displayed as json and as profession
* adjectapproval should be fully working
* fixes to install script, changed default user/profile to guestuser, changed pid in formula.js to look up from db
* install.py, sequencer, schema:
    * made install.py file to set up all db/world/profiles
    * sequencer now supports equals, lt, gt!
    * converted a lot of js schema to py, added environment & settings schema
    * wired up settings to db
* added system status JSON route, added welcome demo button to front page
