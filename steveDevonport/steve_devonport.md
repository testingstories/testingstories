
When is a hero not a hero?

In a previous role I was tasked with creating the Test Automation for a number of different web services, however when I joined the team I quickly discovered that they were lacking the capability to deliver customer value rapidly, securely, or with predictability. All this was compounded by the Scrum ceremonies not being orchestrated and there was no Scrum Master. The technology and tooling side was no better.

After being convinced by the recruitment team and interview process that I would be working with an experienced and high performant group of people the above scenario came as a complete shock, whilst there might be a high performing group of people somewhere in the company...I guess I drew the short straw.

As I saw it I had 2 choices...(1) quit and find a new role or (2) stick around and try to turn the team around.

It's fair to say I chose option 2 otherwise you wouldn't be reading all about my experiences of working with a hero.

As I got to know the people on the team, over the first several months, I put together a list of 'things' that were either missing or just seemed wrong. And so it was that before the end of my probation period I presented my manager with a three pronged approach that would allow us to deliver features transparently, at pace, and with reliability - all within 12 months. A critical consideration to my approach was (1) My Product Owner fully supported the approach and (2) For the first 6 months the team would deliver minimal features into production.

My manager was skeptical of the deadline - not because of my capability (because I'd done this exact thing in a previous role) but because of the people within the team.

So began my journey of unofficial Quality Coach.

The team consisted of a bunch of developers that had lots of experience of writing all the code and then throwing it over the fence, aka they only knew how to deliver changes within a Waterfall process. My challenge was to show them, educate them, and encourage them to take on board the philosophy of Agile and the Scrum methodology in particular. I should add there was a team manager but he was split across several teams and didn't have the time or experience of transforming a team to Agile.

The second part of my approach focused on integrating Test Automation across the soon to be Agile/Scrum delivery lifecycle that the team would adopt. Experience had taught me a big lesson that not getting Test Automation embedded within the entire SDLC would stop all future progress to becoming an agile delivery team. Coupled with this there was the other elephant in the room 'testing is a shared team responsibility' that needed to be tackled quickly and effectively.

The third part of my approach focused on the technologies and tooling for the team and I had assumed the developers would be excited at using shiny new tools, such as: Jenkins, SonarQube, Continuous Delivery, the AWS platform, and so on. I wasn't wrong in my assumption they couldn't get enough, they took all the training courses, all of them completed at least 2 levels of the AWS certification path. All that was missing was how they could create and make use of a Jenkins pipeline and that's where I could step in to help both with the design and initial implementation.

Over the next 6 months I presented multiple workshops covering topics such as: Agile 101, What is Scrum anyway, delivering small pieces of value. Additionally I introduced techniques such as scenario example mapping and story pointing, and so on. I also did a lot of work on breaking down the "It's not my job to write the tests" mindset that was firmly embedded in the team, to help achieve this I introduced the team to the notion of working through the User story and creating Acceptance Criteria using the Gherkin format, we practiced this on a different basis. At no point during these exercies/sessions did I mention the words test coverage, cucumber, or even exploratory.

We get back on track and start to deliver features/changes into production every 2 weeks - at this point we're not ready to deliver customer focused value, but I'm not bothered I need a rest!

Several weeks later 'the management' decide to add an additional engineer to our team, this person was an existing employee coming from an established Agile delivery team, and he already knew our team manager so I thought nothing of it...except that a significant amount of work must be coming our way. 

After a couple of sprints pass by uneventful I take a look at our last Sprint velocity and note that it has shot up dramatically as stories have been brought forward from downstream sprints, this surprised me as I don't remember anyone in any of the ceremonies mentioning it. I mention this change in our velocity during the next retrospective and our new engineer (I think we'll call him Steve) Steve says that he decided to pick stories that he wanted to work on. I looked at the team manager and he shrugged his shoulders and said, 'As Steve is learning about our systems I thought it would be a good learning experience for him.' There was a 'healthy' discussion that consumed the rest of the retrospective!

As time passed and I began building out the Test Automation frameworks, ready for the team to inherit and populate, and the presentations for how we can start to reduce the size of our deliveries into production, I logged on on one evening to get some company branding and noted that Steve was online. So I started a conversation with him. As part of that conversation it transpired that he was working 2-3 nights every week and sometimes the weekend, 'it's the only way I can get the work done' was his defence.

It didn't take too long before other team members start working the odd evening or two in the week and once there were 4 engineers working the weekend.

Naturally this approach broke apart any notion of completing our transition to being a true Agile delivery team.

I spoke to the team manager, privately, about this at some length, stressing how anti-team Steve's approach is. The team manager didn't take too kindly to my 'attack' on his buddy and I was eventually told, "don't be so negative, we're getting the work done aren't we?"

I couldn't deny what the team manager had said to me because it was true we were delivering features into production faster than before and quality was decent enough. But there was no team spirit anymore, people were working crazy hours sometimes starting at 6 or finishing at 10pm, plus weekends. Everyone was getting burned out, especially me as I was writing automated tests for several web services that were being released as a 'big bang'.

This was not how I wanted to work, I was not enjoying how the team was falling back on old ways of working.

As we made the big push, over the weekend, into production and our components came online...nothing worked! With all the rushing and pushing it seems we had missed several integration points across the components...Anyway it took us about a week of head scratching, rework, and long hours going through the server logs to isolate the missing items.

It wasn't too long after that I resigned.