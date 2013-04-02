This week I've made a lot of headway with security stuff, which was my goal for last week.  I learned how to set up protections against CSRF and XSS exploits though I still need to audit the site several times to be thorough.  CSRF is an interesting problem -- having witnessed someone exploit CSRF on someone else's test site as a joke, it's a pretty easy thing to abuse.

I also finally straightened out my user accounts and authentication and how everything interacts with users, their profile settings, and page-to-page interactions.  I had been putting that one off for a while...

I put a lot of time into formulas, which to some degree are the site's secret sauce and will probably require many refactorings.  Right now I am prepping myself for having to do a major refactor on it because it suffers from really bad code smell and is in need of some testing.  This will be good practice code-wise.

The last thing I focused on was converting my old project [AdjectApproval](http://benturner.com/adjectapproval/) over to node.js.  Almost done, though it took longer than I thought.  It will function as another mini-project.

This week I am going to go live with another version of the site (the current public site only has a few routes enabled) so that I can ask some people to hack on it.  I am also thinking of sending some questions around, particularly focused on asking what kind of physical products people would like to have after being shown my Galapag.us business card prototype, and potential pricing for the service since I will have ITP Pitch Fest workshops coming up.  I'm hoping this will be sufficient user testing.

I am also starting to think about what gear to order for the show and thesis week.  I want to dynamically build a business card from the server to show that it can be done, so eventually people can subscribe to monthly/periodic business card shipments.

From github:

* db schema for user settings, mostly done converting adjectapproval from php/mysql to node/mongo
* deleting .pyc files, should be in .gitignore
* formulas, api, schema: added new stats for galapag.us citizenship formula; api routes for credits, personality types; formula sequencer and main page overhaul; changed schema for many stats
* tester profiles now set up correctly, csrf added to login/register
* formula save function complete
* adding csrf token in ajax headers, wireframed profession page for coders
* implemented validator for XSS protection, CSRF protection too; need to add them to whole site
* adding admin dashboard features, also huge update to sessions, req.user
* python script to create new user, should increment redis & mongodb
