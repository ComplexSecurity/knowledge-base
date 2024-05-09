Ffuf is a fuzzer written in the Go programming language. It is an open source [Web Fuzzing](../web/fuzzing.md) tool, intended for discovering elements and content within web applications, or web servers. 

Often when you visit a website you will be presented with the content that the owner of the website wants to serve you with, this could be hosted at a page such as index.php. 

Within security, often the challenges in a website that need to be corrected exist outside of that. For example, the owner of the website may have content hosted at admin.php, that you both want to know about, and test. FFUF is a tool for uncovering those items, for your purusal.

Particularly in the bug bounty scene, a lot of people have gravitated towards **FFUF** since its release. Whilst a good majority of this shift is likely down to the following of the crowd, there is a definite portion of the community who have made the change due to FFUF’s speed, flexibility, and ability to quickly integrate into outside tooling. 

In addition, the maintenance of the project is top notch, especially when compared to compeitive offerings which although similar in features, lack the same passion and speed to market of new features that FFUF has consistently shown. 