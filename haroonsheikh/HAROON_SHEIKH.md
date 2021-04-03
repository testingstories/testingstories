# How technical knowledge leads to productive testing?

A question that arises in most of us during our testing careers is whether testers should be striving to be technical or continue with functional "black-box" testing.

For majority of new testers, the perceived testing career path is Manual/Exploratory testing to Automation to Management whereas the more productive technical career path should be starting as a **Non-technical tester** moving into more **Technical** roles to **Technical leads**.  Being technical does not mean you start coding, but it suggests that we as testers are able to contribute to discussions around building a testable solution with quality-first in mind.

I started my career as a **functional tester** in a completely waterfall team where I was testing a VOIP (Voice over Internet Protocol) based solution with hundreds of pre-written test scenarios.  Soon after a couple of regression cycles, I started to feel that I'm not adding much value to the project when there's a bug found and I'm not able to provide enough information to the developers around the issue and often no contributions in technical discussions around the root cause and solutions.  And we get another version with a fix only to re-start our regression cycle without knowing what was changed/fixed and areas that could be impacted.  I found this extremely limiting as I have always been a tester with a sense of curiosity and asking these "How?", "What-if" and "Why?" questions.

The experience above showed how important it is for a tester to not only understand the requirements of the system-under-test but understanding how the system is doing what it is.  Once acquired some technical knowledge of the system I was testing, was then able to find critical issues as well as gather traces using various tools such as Wireshark to aid in more reproducible bugs.

From first testing role to now a technical tester with variety of experiences, following are few areas I have continuously practiced contributing more productively:

## Knowing the application and test requirements

Whether you're a black-box tester or a white-box tester, it's important to know the requirements of an application to test and it’s even more important to discuss the test requirements.  "What are the test requirements?" has been on top of my "feature/story kick-off" template to discuss during planning how this new feature can be developed with testability in mind.  In my experience, I have found that testable features of an application are easy and less costly to maintain with less regressions.

I have worked on several projects where there are no requirements documented or it's just a "bad requirement" which makes it difficult to test with confidence as there's a bunch of assumptions and no baseline.  When requirements are not clear, it’s good practice to handle these situations with plenty of exploratory testing prioritizing user experience.

## Knowing the technology stack

One area that has helped in getting most amount of test coverage is an understanding of the technology stack without knowing anything about coding.  This enables targeted testing of not only front-end components but also backend technologies including databases.

- It really aids in understanding the inputs and outputs of the system and can easily see where in the automation pyramid a particular test needs to reside.  I.e., Do I really need a test at UI (User Interface) layer when it can easily be covered by a more stable integration/unit test.
- It's important to understand how we can monitor the application behaviour by looking at the logs when an unexpected behaviour occurs at each layer of the stack and helps in tracing the flow or sequence through a system.
- Just knowing the technology can help with identifying potentially interesting variables to explore with testing.  For example, the version of a particular technology used can help with picking on any present security vulnerabilities.  If you're looking to automate testing, then this can also help in deciding what tools and languages to choose for the tests. E.g., If the front-end application is written is `react-js` then writing the integration tests in `testcafe` maybe the preferred to stay in sync with the programming language and shareability of the selectors, etc.

## Knowing the dependencies

Another area of understanding that's helped me shape better tests and healthy conversation with other engineers is the knowledge of dependencies that a system may have on another system.  It could be dependencies within code, between two components or within different requirements.  One way to grasp the connections is by drawing out diagrams of different components of the system, and the communications between them, including the user journeys/interactions between them.  These technical/architecture diagrams can be used for identifying risks, highlight any potential issues earlier in the process, come up with tests that need carrying out, and start thinking about what tools might aid in testing.

When I'm not sure about how a particular feature hangs together technically, then I just ask the developer next to me.

## Pairing with developers

One of most crucial practices of being a technical tester is the ability to pair with the developers.  This does not mean the ability to code but the ability to **read** code.  I like to pair with developers so that we're able to discuss the changes early and have a continuous 3-amigo style conversation throughout to build a more maintainable and testable solution.  I'm able to share my testing perspective to help developers think about those unhappy paths when writing unit tests.  This also encourages discussions around what tests should be covered at which layer of the automation pyramid without repeating ourselves.

Throughout a feature change, I'm adding value by asking a lot of test-related questions and by answering each other, often we would find improvements that could be made to code/solution and find out about risky areas of the changes and produce better and more productive tests early.

I like to also collaborate with the developers when writing the automated functional tests as I believe testing is an activity of the team not just the testers which leads to better coverage and more maintainable tests.

In summary, I would like to stress the importance of having the technical knowledge to test more productively.  Technical skill is a quality highly sought after in testers these days, it's not about whether you're able to create the most efficient automated test framework but it's whether we're able to get involved in technical discussions and give an input from a testing perspective.  We should be able to use this knowledge to derive better test coverage overall and deliver with confidence. Happy testing!

## Author Bio

Haroon Sheikh is a Computer Science graduate from University of Leeds and working proudly as a Senior Test Engineer at Sky. Haroon has a great interest in playground of various testing tools that could be used for aiding in testing workflows.  He believes in the mantra of *Test Automation isn’t a replacement but an aid to gain confidence in quality*.

You can find Haroon on twitter.com/mrhsheikh, connect on linkedin.com/in/mrhsheikh and experiences at terribletester.com.
