This week I made some very good progress!  Not only is my site set up on an EC2 instance, but I also figured out how to buy an SSL certificate, make a key, and configure both NginX and node.js express to use SSL/HTTPS.  So now the server is (at least to some newbish degree) encrypted and verified.  I also got socket.io to work around NginX by being forwarded by Varnish to a listening node.js port.  I don't have a use for socket.io yet but I at least know it works -- I think it might be useful if I can get my games/RPGs up and running.

The other major chunk of my work this week was setting up a dummy database environment for testing.  I've been dreading it for a while but I converted all my mongoose MongoDB models over to python MongoEngine schema.  From there, I can write Python scripts to make fake users and fake entries so I can see what the site will look like with any degree of content.  This will help me test the site and remove as many complications as possible before the first users touch the site.

I also made a welcome "demo" for the quick and dirty thesis and midterm review.  I chose to make a simple page that could be viewed on any device width and let people start thinking about how they could use the site.  I chose to use thanks, good deeds, and a perception survey as introductions into reputation.  I'll show the welcome page on Tuesday for the review and show.

The last thing I did was email [Daniel Suarez](http://en.wikipedia.org/wiki/Daniel_Suarez), author of [Daemon, Freedom (TM)](http://en.wikipedia.org/wiki/Daemon_\(technothriller_series\)), and Kill Decision.  In his books, he wrote about the Daemon and a Darknet, an AI set up by a dead programmer which establishes an alternate economic system for its select group of users.  The users have a Google Glass-like interface and "level up" in their professions (e.g. farming), see quest paths lit up in green lines on their displays, and imbuing physical objects with online-world properties through a sort of augmented reality smithing device.

I received a response from Mr. Suarez, but he's busy at the moment.  I am hoping he might give me some insight into what sorts of things he'd love to see in a real-world version of this Daemon.

From github:

* changed logo, added python models for categories, still need to do dummy entries for testing
* global stats now saving after running python script, fixed some user auth stuff for passport/express
* can now seed db with profiles, need to seed categories next
* saving nicks/nids to redis
* link accounts, switch accounts; both should work?
* filling out wireframes for settings pages
* added settings pages and routes, need to edit them still
* compressed some imgs, wired up confirm/deny buttons on dash
* socketio ssl
* css max width
* https stuff
* need external scripts to be https
* production vs dev server for http/https
* adding testsocketio to demo
* .gitignore fix
* testing ssl server
* auth works, user's profile settings saved to session
* got redis password-protected
* layout fixes for phones
* added nginx, varnish configs; added bonuses/penalties to islands; spam checker for welcome demo
