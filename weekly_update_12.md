This week I bit the bullet and opened up my site for alpha testing.  Basically, I knew this would not attract a massive flood of users, but it was a big thing psychologically I suppose.  It's now out there in the open.  I wrote [a post about it on my own blog](http://blog.benturner.com/2013/04/30/opening-up-galapag-us-for-alpha/).

Overwhelmingly the response has been that people don't know what to do as soon as they reach the first page after user registration.

So I think one of my priorities before thesis is to create some sort of walkthrough tutorial for new users to get them accustomed.  I'm thinking I'll make it in the form of an initial quest for people to complete.

Other than these things, I got socket.io to work for injecting new updates from other users into a person's dashboard.  I also got a github repo issue posted in the ngx_pagespeed repo from Google and their team fixed it (it was a problem with setting caching for the pagespeed beacon and then getting caught by my web front-end Varnish server).  

From github:

* socketio updates to dash and heartbeat pages, found some bugs with religion category
* removed redis listeners, added socketio test for livestreaming, streams show only confirmed stuff
* angularjs topics, some cosmetic fixes to pages, forum route added
* making a couple routes public
* adding some missing routes
* added login link to index page
* fixed display of category objs for receiver anonymous vs. user, added email to profile settings
* fixes to user session settings, ipaddress saved to new objs
* fixes: status bar nicknidpairs and more commands, cleaned up python scripts, removed redundancy, began adding comments, tested via angularjs in tribe page
