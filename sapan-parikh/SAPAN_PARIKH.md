# Not All Tests are the Same

I have gotten an opportunity to work on projects where I learned how automated testing is and that not all automated tests are the same. They differ from each other in at least two ways,speed of execution and risk of failure.

While the testing pyramid is QA 101, it'salso one of the most ignored learning. One project that I worked on depended heavily on unit testing, while the other relied heavily on automated() testing. approaches have their shortcomings.

Approach , which depended solely on unit testing of backend code, had many false positives. In this scenario, the test cases passed all the time. , the software in production did not work. This false assurance could be because of a lack of Javascript tests or 3rd party integration errors because of the limited unit tests.

On the other side, the second approach had precisely the opposite issue. This approach had lots of false negatives. Here many test cases failed, but things were not broken to scale indicated. For instance, 100 broken test cases, or a few percent of test cases always break due to timeouts or other issues not related to the code in production.

This discussion brings us back to the testing pyramid. Any organization or project'stesting strategy should include unit tests, integration tests, Selenium tests, manual tests, etc. Such atest strategy can tell us exactly the problems arewith minimum effort and time.This is how tests differ in size and speed, but they also differ in their impact and risk.It makes sense that when your project is small, you run all the tests, but as it grows, executing all tests may take hours or days. A simple strategy at such times is to distribute your test cases in a quadrant of the likelihoodof failure and impact of failure. A test case with a higher possibility of failure and a high impactisthe kindthat should be prioritized.

Slow running test cases can be given score between 1 to 5 for their possibility of failure and impact of failure. Based on historical data, one can find the probability of the test case failing again. mpact can be based on the possible damage if feature work. The product of both these scores should give us a risk score. Which typically looks like the following:

![Slow running](sapan-parikh/slowrunning.png "Slow Running")

