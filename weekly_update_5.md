In keeping with my schedule, I was able to clone my git repo to my Amazon EC2 instance and get my app running with very minimal edits (I found a few things that needed to be added to my initialization scripts), so perhaps eventually I could very easily spin up a new instance and have everything installed and running with very little extra work.

Since the site is now live in some capacity (nginx serving the frontpage, node.js for certain demo routes), I ran benchmarks on it (EC2 Small) using apache bench:

    Document Length:        20368 bytes
    Concurrency Level:      300
    Time taken for tests:   37.402 seconds
    Complete requests:      5000
    Total transferred:      9497495 bytes
    HTML transferred:       7481687 bytes
    Requests per second:    133.68 [#/sec] (mean)
    Time per request:       2244.142 [ms] (mean)
    Time per request:       7.480 [ms] (mean, across all concurrent requests)
    Transfer rate:          247.98 [Kbytes/sec] received

    Connection Times (ms)
              min  mean[+/-sd] median   max
    Connect:        1   11  37.8      1     290
    Processing:    19 2033 711.3   1977    7375
    Waiting:       19 2018 705.8   1971    7375
    Total:         46 2044 711.2   1983    7377

    Percentage of the requests served within a certain time (ms)
      50%   1983
      66%   2218
      75%   2410
      80%   2494
      90%   2760
      95%   2968
      98%   3329
      99%   3884
     100%   7377 (longest request)`


Caveat: I was running ab off the same instance, to the web site `galapag.us` (e.g. not localhost).

So each request was about 20KB, and I ran 5k requests with 300 concurrent requests.  This might simulate something like 15 users hitting the same page (which has 20 assets on it to download) at the same time.  (15 * 20 = 300)  Despite 300 concurrent requests, there was a mean average of 133/sec.

The times are not that great (over 3 seconds for 2ish% of all the requests) but I also have varnish and nginx serving up the assets, so most of the follow-on requests to my site will be cached.

As I learn more about how to bench my server, I'd like to learn if the slowdowns are coming mostly from the server type, my code, redis (each of those 5k requests had a new session saved as a redis key, as intended), mongo, or something else.  How will it scale when my dbs start having more data in them and I'm doing multiple queries?

This is important to me because I'm beginning to move into a phase where user experience is going to be tested.

I met with my advisor Clay Shirky and talked with Atif this week and both of them really stressed the UX component of my thesis.  The earlier I can get to testing UX, and incorporating feedback (which I'm usually bad at), the better.

Clay mentioned a few things to look at: [Paul Resnick's work on "thanking" and "credit" mechanisms online](http://mail.free-knowledge.org/references/authors/paul_resnick.html), findings from the MIT project Scratch's attempts to automate accreditation for sources and inspiration into code (when in fact children said they wanted to be thanked and acknowledged, not just given automated credit), and danah boyd's research into thanking and crediting.

So, anyway, I'm pretty happy, after all the previous work, to finally have the site running live in some capacity in a fairly modular and technically sound way.

From github:

* added .pyc to .gitignore
* fixed some deployment bugs in newinstance.txt & package.json, index page now in node & not static
* from mongostore to redisstore (need to test sessions)
* added redisstore to package.json
* did some layout for login.html and register.html to prep for user auth
* added redis key profiles:number
* made separate route files for demo vs. actual (see config.js)
* need to continue documenting app structure in README.md
* moved css & js on welcome demo to external files; made new db objs from submitted data & just need to * save it to db now for everything to work
* added deeds; wired welcome demo up to backend, made welcome demo results page already calculated
* added influences & ideas; completed HTML for welcome page/demo