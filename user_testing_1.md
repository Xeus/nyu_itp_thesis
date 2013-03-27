# User Testing Exercise

## What does user testing look like for your project?

I want to nail the on-boarding process, from new account creation to the first few actions one completes as a new member.

So I want to have someone create a new account, verify it, and then begin filling out some information.

The testing will get a little bit into on-boarding so that a new member begins to feel inclusion and investment into the ecosystem.

## Who are your user testers?

The user testers are people who can break a web site.  People with a little knowledge of how to exploit vulnerabilities in a web site, through cookies, CSRF, XSS, data input, etc.

I'm hoping to ask some coder friends and co-workers for help testing, and less technical folks to do the same process but try the introductory pages once they get past user creation and verification.

## What questions are you asking them?

* Create a new account.
* Verify your email.
* Mess with URLs, disable JavaScript, rain chaos onto the server.

## What part of your project are you testing and why?

* Are the appropriate records being set up in the DB when the user creates a new account?
* Are there any roadblocks/bugs/dead-ends when the user is learning how to register?
* Is the server missing obvious protections from commonly-used exploits?
* Will a new user find immediate value in membership by filling out certain information?

## Timeframe?  Phases?

* Process should take 10-20 minutes.

## How are you going to be digesting the feedback?  For redesign?  To use in final presentations?  Short-/long- term utility.

* The feedback will be used to harden the site for this initial user testing, to make sure the integration of several back-end components happens smoothly.
