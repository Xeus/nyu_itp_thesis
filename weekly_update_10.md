This/last week felt like I was solidly in phase 3, user/unit testing.  I figured out how to test the tribes section of my site using mocha, expresso, shouldjs, and assert for nodejs.  I need to test the formula section and general routing around the site, but I've already felt like I've attacked a lot of soupy sections of my code that were leading to mysterious bugs.

I met with Heather on Monday to touch base.  I feel like we're on the same page and Heather's encouragement helped.  We both agreed I need to push myself to begin letting go of Galapag.us and letting it out into the world.

As a result I pushed a big update to the online site -- the routes are still disabled but the server code is updated.  I'll open up routes/accounts later this week.

I managed to recompile nginx with the module ngx_pagespeed, a Google alpha product that does a lot of on-the-fly web page adjustment to make downloads faster on the site.  So my site should be even faster for the general user now.

I had a job interview with the CTO at Happify -- didn't get the job because he needed someone more senior -- but I was very happy to see how happiness and the vocabulary surrounding it is now becoming more common in the startup community.  When I first conceived of the idea in 2006, only economists and positive psychologists (i.e. academics) would be talking about it.

I also pitched Galapag.us at the ITP Pitch Fest.  I think my pitch went well. I managed to make people laugh, felt like I connected with the audience, and I got to pitch to David Tisch and Phin Barnes, who both tend to ask very keen, insightful questions that cut straight to the core of peoples' business ideas.

My task for this week is to open up the site and begin pushing it to the quant self community.  Fingers crossed.

I also need to shift into creating outputs for the formulas being generated on the site.  This means a widget one can put on a site, a business card maker or template, prototype gaming cards.  I also am thinking about how I could have a widget in a browser that recognizes peoples' names on a page and does lookups on their reputations for someone to look at.  This might be a good demo, at the very least.

I really wish I had a couple engineers to approach this in a more structured way.

From github:

* add nicks, tests for add/remove category items 100% green
* email confirm on new account (need to test)
* updating tribes tests for leaving membership
* adjectapproval fix
* font fix
* google web font not displaying right
* adjectapproval array complaining
* removed DEFER from noty scripts
* required npm modules, bug fixes for welcome & adjectapproval
* shutting down routes for the public version
* change to .gitignore
* some fixes to tribe schema, tests 100%, tribes now load default in python script
* whew, massive test building on tribes for pitch tomorrow!
* bugfixing tribes, wireframing adding nicks in settings, some admin controls
* tweaking tribes for pitch fest demo, need to do major bug-fixing though
* added nick list to each category page, extracts it in helpers.buildObj()
* last visitors, edit/fork save correctly, can add another profile now (need to test)
