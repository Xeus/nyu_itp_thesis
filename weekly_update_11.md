This week I opened up Galapag.us's routes but haven't begun telling people about it.  I didn't have enough time to debug, although I fixed a bunch of bugs in the login/registration.  Most of my time this week was spent doing code tests for job interviews, which on one hand was good because A) I need a job and B) I need the practice and C) I've gotten a lot of practice writing tests in QUnit, unittest, and Mocha but was bad because I sorely need to learn more about coding to land a job.

One of my goals for the week was to begin building tools to let Galapag.users show their scores externally.  So I created a bookmarklet that a user can click on in his browser which loads up a little widget on the side of the screen.  The widget searches the page the user is currently on and displays reputation scores for people it finds.  So on this page, it would find a known user, Ben Turner, and display the reputation.  I think it'd be cool to demo this on an ITP page, with a lot of ITPers in the db already.

My goal for this week is to write some baseline tests for the login/registration/user setup parts of my code as well as for the formula code, based on what I've been learning while reading Kent Beck's [Test Driven Development](http://www.amazon.com/Test-Driven-Development-Kent-Beck/dp/0321146530).  Then I need to add some data to the site so that when I demo it, I can show people how a standard happiness formula can be applied easily to a new user.

I've also been reading the docs for angularjs, a front-end framework created by people at Google.  As I need to create a quick and dirty comment system/forum for the site, I may use that as an opportunity to try angularjs out.

All my gear (business cards, large foldout map, t-shirts) arrived in the mail so I'm set up there!

My thesis group gave some good advice for our run-throughs of our presentations.  I re-tooled my presentation and re-ordered some slides so it's in the order that I prefer telling the story in.  I was bumping up against my slides while I was presenting (I told things out of order) so the presentation didn't flow as well as it did for the ITP Pitch Fest (which I guess I got lucky in).

The main task for the presentation is to cut down the length so that I can demo the site more -- most of my feedback revolves around people really needing to see it in action to get what I'm talking about.

From github:

* upgrade mongo instructions added to newinstance.txt, adjectapproval (… …
* bug hunting on adjectapproval
* fixing settings page data
* fix https for api routes, profile now loads for profile settings page
* fixed a bug in profile saving, reason why nids weren't correct
* sanitize takes too long
* tofixed(0)
* widget styling
* fixing avg rep again, fixed widget styling
* https fixes, fixed category Test (was linked to Thanks)
* resettime fix
* throttle reset time
* enabled rate throttling
* bug was site behind pword protection; added try..catch for no html re… …
* fixing weird nidnickpairs redis bug w/ widget
* fix bookmarklet URL to https, fix widget avg reputation inputs
* fixing highcharts libs for https
* fixes to new account + confirm, made widget URLs for galapag.us
* going live with secured routes, crossed fingers here!
* widget now has avg rep per page, some other style fixes
* change genome works
* ip_address now in saved objs from user, change tribe genome
* need to straighten out python scripts, now added widget
