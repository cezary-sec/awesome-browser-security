# Awesome browser security
A curated list of awesome browser security learning material. 

## In-depth introductions
_Where to start?_

* [Chromium security website](https://www.chromium.org/Home/chromium-security/) - lots of useful documents that will paint you a good picture of this highly nuanced domain. 

* [Chrome University](https://www.youtube.com/watch?v=kNzoswFIU9M&list=PLNYkxOF6rcICgS7eFJrGDhMBwWtdTgzpx) (2019) - YT playlist of introductory talks on various aspects of Chromium development. Talks on security, browser's anatomy, mojo, and browser's process are must-have. 
* [High Performance Browser Networking](https://hpbn.co/) (2013) by [Ilya Grigorik](https://twitter.com/igrigorik) - free book on browser networking. 
* _The Tangled Web_ (2011) by [Michal Zalewski](https://twitter.com/lcamtuf) - a bit dated, but still mostly relevant. 
* _The Web Application Hacker's Handbook_ (2011) by Dafydd Stuttard - a bit dated, but interesting. 
* [Public Suffix List (PSL)](https://publicsuffix.org/learn/) - what PSL is and what are its known use cases. 
* [Public Suffix List Problems](https://github.com/sleevi/psl-problems) (2019) by [Ryan Sleevi](https://twitter.com/sleevi_) - excellent article on why PSL should be discontinued. 

### White papers
_Publicly available white papers on browser security._

* [Cure53 Browser Security White Paper](https://cure53.de/browser-security-whitepaper.pdf) (2017) by [Cure53](https://cure53.de/). 
* [X41 Browser Security White Paper](https://browser-security.x41-dsec.de/X41-Browser-Security-White-Paper.pdf) (2017) by [X41 D-Sec](https://x41-dsec.de/). 

## Security challenges

### Memory safety
_Root cause for ~70% of browser's bugs_. 

* [Introduction to Chromium's memory safety](https://www.chromium.org/Home/chromium-security/memory-safety/). 
* [Browser security YT playlist](https://www.youtube.com/playlist?list=PLa-iO6ehPFJhcRggmOu5kUv60vqF9CDOk) by Fuzzing Labs - Patrick Ventuzelo. 

### Spectre
_How Spectre affected browser's security._ 

* Chromium's [Post-Spectre Threat Model Re-Think](https://chromium.googlesource.com/chromium/src/+/master/docs/security/side-channel-threat-model.md). 
* [What Spectre and Meltdown Mean For WebKit](https://webkit.org/blog/8048/what-spectre-and-meltdown-mean-for-webkit/) by [Filip Pizlo](https://twitter.com/filpizlo). 
* [Post-Spectre Web Development](https://www.w3.org/TR/post-spectre-webdev/), W3C First Public Working Draft, 16 March 2021. 
* [A Spectre-shaped Web](https://docs.google.com/presentation/d/1sadl7jTrBIECCanuqSrNndnDr82NGW1yyuXFT1Dc7SQ/edit#slide=id.p) by [Anne van Kesteren](https://twitter.com/annevk). 
* [CORB](https://www.chromium.org/Home/chromium-security/corb-for-developers/). 

### Private Network Access

* [Private Network Access](https://wicg.github.io/private-network-access/), Draft Community Group Report, 23 February 2022. 
* [How to win at CORS](https://jakearchibald.com/2021/cors/) (2021) by [Jake Archibald](https://twitter.com/jaffathecake). 

### XS-Leaks

* [xsleaks.dev](xsleaks.dev). 
* [XSinator.com: From a Formal Model to the Automatic Evaluation of Cross-Site Leaks in Web Browsers](https://xsinator.com/paper.pdf). 
* [Fantastic Timers and Where to Find Them: High-Resolution Microarchitectural Attacks in JavaScript](https://gruss.cc/files/fantastictimers.pdf). 

## How to stay up-to-date

* [Web Application Security Working Group's repo](https://github.com/w3c/webappsec). 
