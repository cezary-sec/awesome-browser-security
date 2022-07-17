# Awesome browser security
A curated list of awesome browser security learning material. 

## 0. Scoping philosophy

The overarching goal of this document is to provide a list of materials to consume to get a good understanding of browser security. 

Contributions are welcome. 

### In scope

* Security of the browser product. 
* Web security issues involving a browser. 

### Out of scope

* Web privacy issues. 
* Server-side web security issues. 

### Preferred sources

* High-quality in-depth introductory materials. 
* Source materials. 
* Important research papers. 

## 1. General introductions
_Where to start?_

* [Chromium security website](https://www.chromium.org/Home/chromium-security/) - lots of useful documents that will paint you a good picture of this highly nuanced domain. 
* [Chrome University](https://www.youtube.com/watch?v=kNzoswFIU9M&list=PLNYkxOF6rcICgS7eFJrGDhMBwWtdTgzpx) (2019) - YT playlist of introductory talks on various aspects of Chromium development. Talks on security, browser's anatomy, mojo, and browser's process are must-have. 
* [High Performance Browser Networking](https://hpbn.co/) (2013) by [Ilya Grigorik](https://twitter.com/igrigorik) - free book on browser networking. 
* _The Tangled Web_ (2011) by [Michal Zalewski](https://twitter.com/lcamtuf) - a bit dated, but still mostly relevant. 
* _The Web Application Hacker's Handbook_ (2011) by Dafydd Stuttard - dated, but interesting. 

### White papers
_Publicly available white papers on browser security._

* [Cure53 Browser Security White Paper](https://cure53.de/browser-security-whitepaper.pdf) (2017) by [Cure53](https://cure53.de/). 
* [X41 Browser Security White Paper](https://browser-security.x41-dsec.de/X41-Browser-Security-White-Paper.pdf) (2017) by [X41 D-Sec](https://x41-dsec.de/). 

### Key concepts

* [Public Suffix List (PSL)](https://publicsuffix.org/learn/) - what PSL is and what are its known use cases. 
* [Public Suffix List Problems](https://github.com/sleevi/psl-problems) (2019) by [Ryan Sleevi](https://twitter.com/sleevi_) - excellent article on why PSL should be discontinued. 
* [RFC6454 The Web Origin Concept](https://datatracker.ietf.org/doc/html/rfc6454). 
* [RFC6265bis Cookies: HTTP State Management Mechanism](https://datatracker.ietf.org/doc/draft-ietf-httpbis-rfc6265bis/). 
* [HTTP State Tokens](https://mikewest.github.io/http-state-tokens/draft-west-http-state-tokens.html) - interesting statement on the tragedy of cookies and how it could be solved. 

## 2. Security challenges and corresponding mitigations

### Memory safety
_Root cause for ~70% of browser's bugs_. 

* [Introduction to Chromium's memory safety](https://www.chromium.org/Home/chromium-security/memory-safety/). 
* [Browser security YT playlist](https://www.youtube.com/playlist?list=PLa-iO6ehPFJhcRggmOu5kUv60vqF9CDOk) by Fuzzing Labs - [Patrick Ventuzelo](https://twitter.com/Pat_Ventuzelo). 

### Spectre
_How Spectre affected browser's security._ 

* Chromium's [Post-Spectre Threat Model Re-Think](https://chromium.googlesource.com/chromium/src/+/master/docs/security/side-channel-threat-model.md). 
* [What Spectre and Meltdown Mean For WebKit](https://webkit.org/blog/8048/what-spectre-and-meltdown-mean-for-webkit/) by [Filip Pizlo](https://twitter.com/filpizlo). 
* [Post-Spectre Web Development](https://www.w3.org/TR/post-spectre-webdev/), W3C First Public Working Draft, 16 March 2021. 
* [A Spectre-shaped Web](https://docs.google.com/presentation/d/1sadl7jTrBIECCanuqSrNndnDr82NGW1yyuXFT1Dc7SQ/edit#slide=id.p) by [Anne van Kesteren](https://twitter.com/annevk). 
* [CORB](https://www.chromium.org/Home/chromium-security/corb-for-developers/). 

### Transport security

* [Mixed content](https://www.w3.org/TR/mixed-content/), W3C Candidate Recommendation Draft, 4 October 2021. 
* [Subresource Integrity](https://www.w3.org/TR/SRI/), W3C Recommendation 23 June 2016. 
* [Upgrade Insecure Requests](https://www.w3.org/TR/upgrade-insecure-requests/), W3C Candidate Recommendation, 8 October 2015. 

### Cross Site Scripting (XSS)

* [Cross-site scripting](https://portswigger.net/web-security/cross-site-scripting) - good introduction to the problem. 
* [Content Security Policy 1.0](https://www.w3.org/TR/CSP1/), W3C Working Group Note 19 February 2015. 
* [Content Security Policy Level 2](https://www.w3.org/TR/CSP2/), W3C Recommendation, 15 December 2016. 
* [Trusted Types](https://w3c.github.io/webappsec-trusted-types/dist/spec/), Editor’s Draft, 1 June 2022. 
* [HTML Sanitizer API](https://wicg.github.io/sanitizer-api/), Draft Community Group Report, 13 July 2022. 

### Cross Site Request Forgery (CSRF)

* [Cross-site request forgery (CSRF)](https://portswigger.net/web-security/csrf) - good introduction to the problem. 
* [RFC6265bis Cookies: HTTP State Management Mechanism](https://datatracker.ietf.org/doc/draft-ietf-httpbis-rfc6265bis/) - particularly section on SameSite attribute. 

### Cross Site Leaks (XS-Leaks)

* [xsleaks.dev](xsleaks.dev). 
* [COOP and COEP sections in the HTML Living Standard](https://html.spec.whatwg.org/multipage/origin.html). 
* [XSinator.com: From a Formal Model to the Automatic Evaluation of Cross-Site Leaks in Web Browsers](https://xsinator.com/paper.pdf). 
* [Fantastic Timers and Where to Find Them: High-Resolution Microarchitectural Attacks in JavaScript](https://gruss.cc/files/fantastictimers.pdf). 

### Private Network Access

* [Private Network Access](https://wicg.github.io/private-network-access/), Draft Community Group Report, 23 February 2022. 
* [How to win at CORS](https://jakearchibald.com/2021/cors/) (2021) by [Jake Archibald](https://twitter.com/jaffathecake). 

## How to stay up-to-date

* [Web Application Security Working Group's repo](https://github.com/w3c/webappsec). 
