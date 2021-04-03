# How technical knowledge leads to productive testing?

A question that arises in most of us during our testing careers is whether testers should be striving to be technical or continue with functional "black-box" testing.

For majority of new testers, the perceived testing career path is Manual/Exploratory testing to Automation to Management where as the more productive technical career path should be starting as a **Non-technical tester** moving into more **Technical** roles to **Technical leads**.  Being technical does not mean you start coding but it suggests that we as testers are able to contribute in discussions around building a more testable solution with quality-first in mind.

I started my career as a **functional tester** in a completely waterfall team where I was testing a VOIP (Voice over Internet Protocol) based solution with hundreds of pre-written test scenarios.  Soon after a couple of regression cycles, I started to feel that I'm not adding much value to the project when there's a bug found and I'm not able to provide enough information to the developers around the issue and often no contributions in technical discussions around the root cause and solutions.  And we get another version with a fix only to re-start our regression cycle without knowing what was changed/fixed and areas that could be impacted.  I found this extremely limiting as a tester in terms of how well the quality has been maintained.

The experience above showed how important it is for a tester to not only understand the requirements of the system-under-test but understanding how the system is doing what it is. Once acquired some technical knowledge of the system I was testing, was then able to find critical issues as well as gather traces using various tools such as Wireshark to aid in more reproducible bugs.

From first testing role to now a technical tester with variety of experiences, following are few areas I have continuously practiced to contribute more productively:

## Knowing the application and test requirements

Whether you're a black-box tester or a white-box tester, it's important to know the requirements of an application to test and its even more important to discuss the test requirements.  "What are the test requirements?" has been on top of my "feature kick-off" templates to discuss in planning how this new feature can be developed with testability in mind.  In my experience, I have found that testable features of an application are easy and less costly to maintain with less regressions.

I have worked on several projects where there are no requirements documented or it's just a "bad requirement" which makes it difficult to test with confidence as there's a bunch of assumptions and no baseline.  When requirements are not clear, It's good practice to  handle these situations with plenty of exploratory testing prioritizing user experience.

## Knowing the technology stack

One area that has helped in getting most amount of test coverage is an understanding of the technology stack.  This enables targeted testing of not only front-end components but also backend technologies including databases.  It really aids in understanding the inputs and outputs of the system and can easily see where in the automation pyramid a particular test needs to reside.  I.e. Do I really need a test at UI (User Interface) level when it can easily be covered by a more stable integration/unit test. Moreover, understanding of the tech stack could help or impact with testing things like:

- Monitoring of the logs when an unexpected behavior occurs at each layer of the stack
- Knowing the technology can help you identify potentially interesting variables to explore with testing.
- Knowing the technology can help you identify limitations and vulnerabilities of the technology. Knowing those things, you can write tests to explore how the system deals with those limitations and vulnerabilities

## Know the code bases

```
- It's not about coding, it's about reading the code.

```

## Pairing with developers

## Know the dependencies

## Know the requirements

## About the author

Haroon Sheikh is a Computer Science graduate from University of Leeds and working proudly as a Senior Test Engineer at Sky. Haroon has a great interest in playground of various testing tools that could be used for aiding in testing workflows.  He believes in the mantra of *Test Automation isn’t a replacement but an aid to gain confidence in quality.*.

You can find Haroon on twitter.com/mrhsheikh, connect on linkedin.com/in/mrhsheikh and experiences at **[terribletester.com](http://terribletester.com/)**.
