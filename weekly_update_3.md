Finished an overhaul of the core category backend, which will let me add in new categories (faves, pets, foods) easily and have them show up throughout the system dynamically.  I also run each added entry through a filter system so it can check to see if everything's valid, and then returns a notification message to the client.  Now I can work on other features on the site more freely, without worrying about the underlying systems.

Other thing I did was do some early benchmarking of the server.  I tried using `apache bench` on an Ubuntu VirtualBox instance via my Windows 7 PC, connecting to node.js on my MacBook Air.  I heard that OSX doesn't run node.js so well, and I had pretty disappointing results (only about 100-150 connections before errors popped up, and wait times in extreme cases above 10 seconds).  I also tested against my Ubuntu system and was getting no errors at very high load (1000 concurrent connections).  So I think node.js will run better once it's on an Amazon EC2 instance (I have an EC2 small set up already, with nginx and varnish in front of everything, which will help handle requests faster).  I'm doing all this because I do believe in the Google mantra that a faster, more responsive web site is more sticky and fun to use.  Anything over a second or two per request makes the site less enjoyable.

Here's my project updates:

From github:

* added bests, hates, worsts, some logic to display top frequency categories on category template pages
* perception stats/formulas almost done but not tested
* moved out old category pages, quest button now works, made status bar simpler
* fixing category page additions & proper JSON messages
* major re-factoring attempt for category pages

Other:

* Received email from [John Havens](https://twitter.com/johnchavens) of [Happathon](http://socialmediaweek.org/newyork/events/?id=49156), both of us interested in reputation and a happiness economy.  Will meet him next week before Social Media Week event.