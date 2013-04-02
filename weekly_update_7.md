This update includes work from Spring Break week, in which I went to Hawai'i and did no work for 7 nights.  Woohoo!

Before the break, I solidified the welcome demo for the midterm presentation.  No crashes for the whole process, thankfully.  Got some good feedback, mostly for improving the slide presentation.

So far I've received 7 user submissions for the welcome demo (including my own).  The answers I got were very open and detailed.  I received feedback that the questions asking for examples of thanks owed to others, thanks received, self-perceptions, and memorable deeds were very challenging.

The people who submitted info were invested in helping out for one reason or another so this skews the results, but I do think that having people invest more into social networks can be a good way towards building a better community for them, and for forming deeper relationships with both the technology and the people interacting online.  I also feel that framing an experience around thinking about one's deeds towards others and vice versa is exactly the tone I want to set and gives more value towards being a considerate person within a community and society.  In this way I feel like the welcome demo and small user testing has imbued my project with a bigger sense of finding my own voice and some sort of artistic meaning.

I think the difficulty of filling out info on the site, then, will be off-set if I can show that the investment of time and introspection pays off with an exponential increase of value once people can look at all of their data combined with it, and in the context of everyone else's public responses.

Since I was on vacation I couldn't attend the NYC Happathon on UN Global Happiness Day, though I imagine the Happathon was a lot like the event held for Social Media Week.  I did fill out [the online happathon survey](http://happathon.com/survey/) though.

Some theoretical hindrances I'm running into:

* For occupations and leveling/achievements for them, I'm having some trouble thinking about how one would come up with universally-agreed qualifications.  So, if you are working on leveling up your "accounting" skill, what does that mean?  Obviously getting a degree or MBA would offer big points.  What about years at an accounting firm?  Becoming a CPA?  But what about more granular results?  What if you wanted to level up as, say, a construction worker?  Or a librarian?  Or a restaurant manager?  How can you begin to quantify that in a way that it's universal?  I feel if I can nail this part, then it'd be HUGE for résumés, an area I definitely want to blow out of the water in terms of accurately representing someone's skills, potential, and goals.
* Standard Galapag.us formulas.  So I want people to be able to build their own formulas to quantify aspects of their lives, but for sure I want to have a standard list of formulas that I can compare everyone on the site with.  So I need to use my formula creator (called the "sequencer"), which works by the way (!), to come up with these standards.  I have this on my schedule to complete last week and this week.  It's my major undertaking and if I can come up with reasonable formulas, then I'll have broken through a wall I've had for years.  That said, it's going to involve adding a lot more variables into the system, which means adjusting my database schema and Python scripts and such.
* Tests.  I'm excited about writing tests for the server because I like hardening systems in general and because I want more experience doing it.  When you write tests, they force you to separate your code logic into discrete parts, which I think will make me a better coder.  The problem is that I really don't think I should spend too much time "testing" at this point when I'm trying to build out something that people can actually use -- especially if, on the face of it, things seem to be working fine enough now.  I just know that a proper engineer writes solid tests.

Other than those, I feel like I'm pretty much on schedule.  I want to have more time at the end to create some experimental widgets/sites to expose people to what could be possible on galapag.us.  For instance, I created [Adject Approval](http://benturner.com/adjectapproval/) over my 1st year winter break.  Looks like a spammer found it recently but it does work well.  It basically let you enter in a person along with adjectives you'd use to describe him, and/or then guess who a person is based on descriptive words.  I'm going to port this over to galapag.us (it's in PHP/MySQL, so I'd have to convert it to JavaScript/MongoDB).

I have bits and pieces of a lot of different parts of the site working, and as more pieces come together, then I can begin tightening the screws.  I wish I could complete pieces in full first, but the good thing is that it's allowed me to flexibly modify parts as their requirements have grown.

At the very least, this thesis project has been an awesome experience in terms of project management, time management, and crash-coursing in coding!

Commits from github:

* python script to create new user, should increment redis & mongodb
* admin user control (still need to link it to user visibility/access to site)
* wireframe site prefs page; laying out developer section
* adding more individual-level stats
* improving & debugging sequencer, added individual-level stats to sequencer
* debugging formula sequencer & routes
* started API documentation page w/ styling
* randomizes order of thanks/deeds
* brighter text on demo
* more style fixes
* fixing spam checker
* added google analytics to welcome demo
* more style fixes, done now
* style fixes for demo based on user feedback
* style fixes to demo
* fixed welcome demo so it saves before doing queries
* python script to add dummy entries, still needs some tweaking for testing but ok for now
* page width fix
* remove some fields from demo
* .gitignore
* added config.py to .gitignore
