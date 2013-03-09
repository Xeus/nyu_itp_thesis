This week I hooked up a lot of the front-end interface to node.js and to the database, with proper responses handling the transaction.  The framework for the world (islands, weather patterns, island bonuses, animals) is linked to the front-end now -- I need to wait for other parts of the system to come online before I go further on these parts, since they rely on the volume and richness of user-contributed data.

I went to the initial H(app)athon event at 92Y for Social Media Week and talked to a couple people on the happiness survey's panel.  Very good discussions.  Everyone there gets it.  I listened to John Clippinger talk about his current work, mostly with the Mustard Seed Project, for creating a social stack that can allow for personal data control but also expressiveness of data within the internet's much-needed social layer.  Self-actualization was a key theme -- the prevalent belief is that happiness metrics as a movement must spring organically from the bottom on up, and not as a top-down metric, even though the United Nations and World Economic Forum were present at the event to support the movement.

I told Heather this, but I feel like since I started thinking about this in 2006, the literature and vocabulary has been developed around the topic since then, so that now we're beginning to see a movement emerge, and connections being made among quant selfers, happiness/gifting/social capital economists, and technologists.  The pump is being primed.  I hope to be in the right place when it takes off.

Final note.  I met with Heather one-on-one to talk about thesis.  We compared notes about the process of going through thesis and dealing with finding work-life balance in crisis management/international development and forging one's career reputation.  We also bonded over Georgetown and tennis.  I feel like Heather gets what I'm trying to do and why it's important to me, and that's extremely important support-wise.  Thanks, Heather!

From github:

* about page
* genome/profile page formatting, added culture & bonuses to islands, cleaned up layout.html styling
* added total global stats, edits to layout/status bar, added some lists to categories
* added reviews category, linked_accounts field in profile model
* perceptions surveys now editable, enterable, more stats available, new categories (wants, obstructions, goals) added
* user genome/profile now hooked up to db
* added global map, added global stats models in py and js, added global stats to sequencer
* individual island pages now show stats, profile now has access to full profile data
* added tests category, added labels to add-category, cleaning up dashboard & profile
* fixed bug in adding animals via python, showed frequency counts to animals on each island, fixed formatting on map, perceptions
* island descriptions added, added all categories to formula page, formulas validate too
