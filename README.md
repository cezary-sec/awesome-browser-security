# Awesome browser security
A curated list of awesome browser security learning material. 

## 0. Scoping philosophy

The overarching goal of this document is to provide a list of materials to consume to get a good understanding of browser security. 

Contributions are welcome. Please file one PR per change. 

### In scope

* Security of the browser product. 
* Web security issues involving a browser. 

### Out of scope

* Web privacy issues. 
* Server-side web security issues. 

### Preferred sources

* High-quality, in-depth introductory materials. 
* Source materials. 
* Important research papers. 
* Docs available online for free. 

## 1. General introductions
_Good starting points._

* [Chromium security website](https://www.chromium.org/Home/chromium-security/) - lots of useful documents that will paint you a good picture of this highly nuanced domain. 
* [Chrome University](https://www.youtube.com/watch?v=kNzoswFIU9M&list=PLNYkxOF6rcICgS7eFJrGDhMBwWtdTgzpx) (2019) - YT playlist of introductory talks on various aspects of Chromium development. Talks on security, browser's anatomy, mojo, and browser's process are must-have. 
* [Web Browser Engineering](https://browser.engineering/) by [Pavel Panchekha](https://pavpanchekha.com/) & [Chris Harrelson](https://twitter.com/chrishtr). 
* [High Performance Browser Networking](https://hpbn.co/) (2013) by [Ilya Grigorik](https://twitter.com/igrigorik) - free book on browser networking. 
* _The Tangled Web_ (2011) by [Michal Zalewski](https://twitter.com/lcamtuf) - a bit dated, but still mostly relevant. 
* _The Web Application Hacker's Handbook_ (2011) by Dafydd Stuttard - dated, but interesting. 

### Architecture
_How browser's architecture supports security._

* [The Security Architecture of the Chromium Browser](https://seclab.stanford.edu/websec/chromium/chromium-security-architecture.pdf) (2008). 
* [Mojo](https://chromium.googlesource.com/chromium/src.git/+/master/mojo/README.md). 

### Security assessments
_Publicly available security assessments of browsers._

* [Cure53 Browser Security White Paper](https://cure53.de/browser-security-whitepaper.pdf) (2017) by [Cure53](https://cure53.de/). 
* [X41 Browser Security White Paper](https://browser-security.x41-dsec.de/X41-Browser-Security-White-Paper.pdf) (2017) by [X41 D-Sec](https://x41-dsec.de/). 

### Key concepts
_Formal definitions, known issues, state-of-the-art._

* [Public Suffix List (PSL)](https://publicsuffix.org/learn/) - what PSL is and what are its known use cases. 
* [Public Suffix List Problems](https://github.com/sleevi/psl-problems) (2019) by [Ryan Sleevi](https://twitter.com/sleevi_) - excellent article on why PSL should be discontinued. 
* [RFC6454] Barth, A., "The Web Origin Concept", RFC 6454, DOI 10.17487/RFC6454, December 2011, <https://www.rfc-editor.org/info/rfc6454>.
* [RFC6265] Barth, A., "HTTP State Management Mechanism", RFC 6265, DOI 10.17487/RFC6265, April 2011, <https://www.rfc-editor.org/info/rfc6265>.
* [RFC6265bis] Chen, L., Englehardt, S., West, M., Wilander, J., "Cookies: HTTP State Management Mechanism", <https://datatracker.ietf.org/doc/draft-ietf-httpbis-rfc6265bis/>. 
* [HTTP State Tokens](https://mikewest.github.io/http-state-tokens/draft-west-http-state-tokens.html) - interesting statement on the tragedy of cookies and how it could be solved. 

## 2. Security challenges and corresponding mitigations

### Memory safety
_Root cause for ~70% of browser's bugs_. 

* [Introduction to Chromium's memory safety](https://www.chromium.org/Home/chromium-security/memory-safety/). 
* [V8 Sandbox - External Pointer Sandboxing](https://docs.google.com/document/d/1V3sxltuFjjhp_6grGHgfqZNK57qfzGzme0QTk0IXDHk/edit#heading=h.xzptrog8pyxf) (2022)  - new hardening measures for V8. 
* [MiraclePtr One Pager](https://docs.google.com/document/d/1pnnOAIz_DMWDI4oIOFoMAqLnf_MZ2GsrJNb_dbQ3ZBg/edit) (2021). 
* [MiraclePtr The UaF Slayer [BlinkOn 16]](https://www.youtube.com/watch?v=WhI1NWbGvpE) (2022). 
* [PartitionAlloc Design](https://chromium.googlesource.com/chromium/src/+/master/base/allocator/partition_allocator/PartitionAlloc.md). 
* [Experimenting with Rust in Chromium](https://chromium.googlesource.com/chromium/src/+/refs/heads/main/docs/security/rust-toolchain.md). 
* [Retrofitting Temporal Memory Safety on C++](https://security.googleblog.com/2022/05/retrofitting-temporal-memory-safety-on-c.html) (2022). 

### Spectre
_How Spectre affected browser's security._ 

* Chromium's [Post-Spectre Threat Model Re-Think](https://chromium.googlesource.com/chromium/src/+/master/docs/security/side-channel-threat-model.md). 
* [What Spectre and Meltdown Mean For WebKit](https://webkit.org/blog/8048/what-spectre-and-meltdown-mean-for-webkit/) by [Filip Pizlo](https://twitter.com/filpizlo). 
* [Post-Spectre Web Development](https://www.w3.org/TR/post-spectre-webdev/), W3C First Public Working Draft, 16 March 2021. 
* [A Spectre-shaped Web](https://docs.google.com/presentation/d/1sadl7jTrBIECCanuqSrNndnDr82NGW1yyuXFT1Dc7SQ/edit#slide=id.p) by [Anne van Kesteren](https://twitter.com/annevk). 
* [CORB](https://www.chromium.org/Home/chromium-security/corb-for-developers/). 

### Transport security
_Mitigating active and passive network attackers._

* [Certificate Transparency in Google Chrome: Past, Present, and Future](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9592820) (2021). 
* [Mixed content](https://www.w3.org/TR/mixed-content/), W3C Candidate Recommendation Draft, 4 October 2021. 
* [Subresource Integrity](https://www.w3.org/TR/SRI/), W3C Recommendation 23 June 2016. 
* [Upgrade Insecure Requests](https://www.w3.org/TR/upgrade-insecure-requests/), W3C Candidate Recommendation, 8 October 2015. 

### Cross Site Scripting (XSS)
_Attacks on the integrity of JavaScript code._

* [Cross-site scripting](https://portswigger.net/web-security/cross-site-scripting) - good introduction to the problem. 
* [Content Security Policy 1.0](https://www.w3.org/TR/CSP1/), W3C Working Group Note 19 February 2015. 
* [Content Security Policy Level 2](https://www.w3.org/TR/CSP2/), W3C Recommendation, 15 December 2016. 
* [Trusted Types](https://w3c.github.io/webappsec-trusted-types/dist/spec/), Editor’s Draft, 1 June 2022. 
* [HTML Sanitizer API](https://wicg.github.io/sanitizer-api/), Draft Community Group Report, 13 July 2022. 

### Cross Site Request Forgery (CSRF)
_Abusing cookie-based session management to forge requests._

* [Cross-site request forgery (CSRF)](https://portswigger.net/web-security/csrf) - good introduction to the problem. 
* [RFC6265bis] Chen, L., Englehardt, S., West, M., Wilander, J., "Cookies: HTTP State Management Mechanism", <https://datatracker.ietf.org/doc/draft-ietf-httpbis-rfc6265bis/> - particularly section on SameSite attribute. 

### Cross Site Leaks (XS-Leaks)
_Using side channels to leak bits of data cross-site._

* [xsleaks.dev](https://xsleaks.dev) - one stop shop for XS-Leaks. 
* [COOP and COEP sections in the HTML Living Standard](https://html.spec.whatwg.org/multipage/origin.html). 
* [XSinator.com: From a Formal Model to the Automatic Evaluation of Cross-Site Leaks in Web Browsers](https://xsinator.com/paper.pdf). 
* [Fantastic Timers and Where to Find Them: High-Resolution Microarchitectural Attacks in JavaScript](https://gruss.cc/files/fantastictimers.pdf). 

### Extensions
_Security of the extension ecosystem._

* [An Evaluation of the Google Chrome Extension Security Architecture](https://www.usenix.org/system/files/conference/usenixsecurity12/sec12-final177_0.pdf) (2012). 
* [Cursed Chrome](https://github.com/mandatoryprogrammer/CursedChrome) - a Chrome-extension implant that turns victim Chrome browsers into fully-functional HTTP proxies. By using the proxies this tool creates you can browse the web authenticated as your victim for all of their websites. 

### URL bar security
_Users must know which website is displayed._

* [Internationalized Domain Names (IDN) in Google Chrome](https://chromium.googlesource.com/chromium/src/+/main/docs/idn.md). 

### Private Network Access
_Abusing browsers to attack private networks._

* [Private Network Access](https://wicg.github.io/private-network-access/), Draft Community Group Report, 23 February 2022. 
* [How to win at CORS](https://jakearchibald.com/2021/cors/) (2021) by [Jake Archibald](https://twitter.com/jaffathecake). 

## 3. Attacks on browsers 
_Fuzzing and browser exploitation._

* [OffensiveCon22 - Samuel Gross and Amanda Burnett - Attacking JavaScript Engines in 2022](https://www.youtube.com/watch?v=FK2-1FAbbXA) (2022). 
* [Browser security YT playlist](https://www.youtube.com/playlist?list=PLa-iO6ehPFJhcRggmOu5kUv60vqF9CDOk) by Fuzzing Labs - [Patrick Ventuzelo](https://twitter.com/Pat_Ventuzelo). 
* [In-the-Wild Series: Chrome Exploits](https://googleprojectzero.blogspot.com/2021/01/in-wild-series-chrome-exploits.html) (2021) by Sergei Glazunov. 
* [Awesome browser exploit](https://github.com/Escapingbug/awesome-browser-exploit) (last update 2020) - collection of various materials on browser exploitation. 

## 4. Misc

* [Web Application Security Working Group's repo](https://github.com/w3c/webappsec). 
* [Browser security research](https://github.com/security-prince/Browser-Security-Research/). 

## 5. Contributors

* [Diego Porras](https://www.linkedin.com/in/daporras/). 
* Łukasz Bendig. 
