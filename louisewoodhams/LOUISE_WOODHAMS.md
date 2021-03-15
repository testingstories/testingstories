# Swagger Like Jagger - A REST API Testing Story By Louise Woodhams

Hi, I'm Louise. I'm a tester of just over 5 years. In my time I've encountered a couple of REST APIs (and some SOAP ones). I really enjoy this kind of testing. I wanted to share the experiences 
I've had and possibly some tips that might help you.

## APIS - Those Are Things 

When I started testing APIs I had no idea what they were and for a fair chunk of that time I wouldn't have been able to give you a decent definition. 
They were middle men to me. The API I was testing was primarily built to sit between a system I knew very well and various external customer systems. This API ended up supporting lots of different types of external customer setups, requirements and acted in a bunch of ways like a translator between them so I tried to translate it into something I understood.

## Context Is King 

This is how I managed to test this API without really understanding what it was. As a tester context vital and if I can find a way to relate the unknown scary thing to something I've tested or 
experienced before it becomes more manageable. I am usually terrible at asking questions but for this project I asked for context and it really helped. I kept drawing on the system I already knew and 
investigated the customer configuration that would be used with this API to build true to life testing scenarios. This actually found some decent bugs and some holes in the UNIT testing and original setup.


## Swagger Training Wheels 

The development team had thankfully added a swagger to the API I was interacting with. I love a Swagger. It is a great place to start with API testing. If it is built right (I'll go into this more later) you can gain an understanding pretty quick, consider a bunch of test cases in advance and actually import it into a postman collection which with some tweaks is usable from the get go. 
Swaggers are colourful. I think these colours helped me learn REST APIs quicker. Swagger supplies you with example requests with the JSON all right there as well as the expected responses.  
Swagger flag up fields that are mandatory. Header fields are separate so you can be aware of differences and adapt these into your test plans. you could eventually create postman test collections. 
Swaggers can handle different types of authentication. They can deal with tokens etc for different customers even within the same Swagger page, if set up correctly. A Swagger is fantastic training wheels for you to find your feet testing an API and once you feel comfortable you can start poking holes in it.  

## The Swagger Is Not Gospel 

As useful as the Swagger is like anything else you test can't always be trusted. You need to remember that. I recommend if it has authentication trying every call and checking for 401s : Unauthorized. Once authorized try that again. Check how mandatory those fields are. Check the 200s 204s are coming back as expected. They should handle duplicate requests (for things like account creations) in PUTs or POSTs. Each Swagger should have details of the responses that you are expecting to get when you send on a request. This list was built by whomever created the Swagger is an is not necessarily complete.


## JSON And His Bracketnauts 

With API testing you'll probably be writing a bunch of JSON. If you haven't had much exposure to coding at this point you'll probably have the problem I had which was you'll mess up your braces {} or miss off a comma or a bracket [] for an array as you just aren't use to using them or you copy pasted from Notepad++ and missed a bit off. This is one of the places Swagger falls down as well. Within the "Try It Out" boxes with the example code you can remove things by accident when adding in your test responses and it will just give you a 400: Bad Request with little to no reason as to why. It is really hard to work out where you've gone wrong and sometimes it is because you've 
copy and pasted in from a PBI/Story/item and it has added a bunch of random spaces which you can't see. I have a tip for you here. Copy paste it into Postman or VS code. Both will tell you where you've gone wrong and highlight where you need to fix things. If you still get a 400 after this then what you are sending as data might not be right.


## Validation And Required Fields 

Validation and Mandatory fields / boxes will be a thing you will have probably come across during your testing journey or just in you day to day with the apps you use or rely on. In my experience however they do tend to get forgotten about by developers when they knock up an API. Typically not supplying things for mandatory / required fields should give you a ticket to 400: Bad Request Ville but this is usually a great opportunity to cause some explosions and get some 500s where validation has been missed or you're sending something unexpected.

## HTTP Codes And Checking For Teapots 

I'm a major geek about HTTP Codes because of the API testing I've done over the years. The full list of there is here: https://developer.mozilla.org/en-US/docs/Web/HTTP/Status and I'll explain a couple that 
have brought me joy and sadness. Most of the time you will want to be getting things in the 200 range depending if data is coming back or not and depending on the kind of data that was supplied in the first place.
I haven't encountered many 300s in my API testing time but I haven't tested a massive range of APIs. The 300 range deals with redirection. The 400 range deals with errors. This can either be caused by a lack 
of permission your side in relation to what you are sending or a lot of the time your authentication has timed out but sometimes the admin you are authenticated as doesn't have permission to do that (a DELETE for example). Other
times it is due to the Request type being wrong, you could be sending your request as a GET and it is supposed to be a POST 405: Method Not Allowed. My favourite of the 400s is 418: I'm A Teapot and 
I recommend if you are involved in building an internal REST API you encourage your development team to build in a legit 418, bonus points for custom error messages and Postman tests!

 ## The Joys of 500s And How You Should Never See Them 

This is where my HTTP code geekiness shows even more. I love getting 500s when testing APIs. I will do a little victory dance, terribly unprofessional I know. 500, known to its friends as Internal Server Error means 
you hit the API so hard it fell over and had a little cry or which I mentioned previously, you did something the developer who wrote the API didn't expect. This is QA bread and butter, these are the 
bugs/errors we live for right? I am of the mind you should NEVER see a 500 in the API you are testing regardless. I have argued this with developers it should be able to handle whatever you send and it 
if can't it should supply a 400 Bad or something in the 400 range. They should never be created and used on purpose. 500 is just not ok which is why they make me so happy when I find them.


## Postman 🚀

I mentioned Postman briefly earlier on. Honestly, when I first started testing APIs, I installed it (https://www.postman.com/downloads/) set it to darkmode and went back to the Swagger as I found it too overwhelming. 
If the API you are testing is simple or you can't get on with Swagger, Postman is the way to go. 
I love using Postman now and not only for how easy it makes everything but it is a great place to store little API calls you only use occasionally and a fantastic playground to set up a API test collection that you could eventually add into your pipeline. It has amazing scope for writing tests with a wealth of test code snippets and environment options to help you along the way. 
It handles everything Swagger does in an easier to use way with more future potential but first time it can be too much in one go. 
 

## Mocking And Shouting BEES Beeceptor🐝

During my time API testing, other than 500s the thing that has bought me the most joy is Beeceptor https://beeceptor.com/. Similar to Mocky, Beeceptor allows you to stand up a URL Endpoint to intercept your requests and send on any custom response you want.  It doesn't require much setup and is a great way to mock a client request or help check a process beyond your API will work. I had to use this frequently for the first API I tested. It had a lot of moving parts and required notification functions to be run for to local systems. It often took me a while to set everything up and trial and error but when the notifications came through to Beeceptor and it sent on its message I couldn't help but shout "BEES" in glee. After months of this me and Beeceptor are firm friends. It even helped me with a rather unpleasant SOAP API process I had to debug.

## When It Gets SOAPY And Final API Thoughts

I feel unlucky as I have had to deal with SOAP a few times in my career. It is REST APIs shameful older brother and the less said about it the better. It has its own rules for error handling and isn't really a fan of being helpful in anyway in my experience. SOAP requests are in XML which is not much fun to write either and must easier to get wrong.

I hope some of the things I have said have been useful or at least given you a solid place to start with your REST API testing journey.  You now know a little more at least and most of all feel more prepared to tackle an API if a wild one appears and casts confusion, it won't be super effective. I am by no means an expert but all experience, good or bad helps shape us and any knowledge we can pass on can be useful one way or another. 




