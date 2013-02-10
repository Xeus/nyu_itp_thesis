# Progress Update: Week #2

From github:

Accomplished a lot this week.  Managed to solidify and get working an entire process from user input through the server down to redis & the Mongo database and then sending the status messages back up to the user via notifications.  With this done, now I can work on higher-level features.  The low-level is now mostly solid, save for writing tests and adding identity switching.

* got streams working finally, just need to extend them across all category pages
* added noty for system notifications, faves.html is testbed for addition logic, pid_receiver added to all models
* wireframe of identity switch dropdown, added 'status' to all models for confirm/deny functionality
* moved achievements to unlocks, added quests, partially implemented confirmdeny but need to finish it
* added DATALIST lists to category pages
* added some aggregate stats, added json route for island stats, added personal stream to profile/genome page
* redis keys for island stats, animals, displayed on /map route, global search now accepts Return key
* massive overhaul of category pages, whew!
* partially thru redoing routes (again)
* added skills.js routes
* added religion page, fixed add routes so they're less reliant on model schema
* fixed routes, views, models for addable items; added a bunch of categories; API route for US states

Other stuff:

* I'm going to the H(app)athon for Social Media Week on Tuesday. 
* Didn't make it into TechStars NYC for Galapag.us.  Bummer.
