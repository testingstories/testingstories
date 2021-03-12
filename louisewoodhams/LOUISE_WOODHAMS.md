# Swagger Like Jagger - An REST API Testing Story By Louise Woodhams

## APIS - Those Are Things 

When I started testing REST APIs I have no idea what they were and for a fair chunk of that time I wouldn't have been able to give you a decent definition.  
They are a middle man to me and the API I was primarily testing was built to sit between a system I knew very well and an external client system.  
It acted in a bunch of ways like a translator so I tried to translate it into something I understood.  

## Context Is King 

This is how I managed to test this API without really understanding why it was a thing. As a tester I find context vital and if I can find a way to relate the unknown scary thing to something I've tested or 
experienced before it becomes more manageable. I am usually terrible at asking questions but for this project I asked for context and it really helped. I kept drawing on the system I already knew and 
investigated the client configuration that would be used with this API to build true to life testing scenarios. This actually found some decent bugs and some holes in the UNIT testing.  


## Swagger Training Wheels 

The development team had thankfully added a swagger to the API I was interacting with. I love a swagger. It is a great place to start with API testing. If it is built right (ill go into this more later) you can gain an understanding pretty quick, consider a bunch of test cases in advance and actually import it into a postman collection which with some tweaks is usable from the get go. 
Swaggers are colourful. I think these colours helped me learn and retain REST APIs quicker.  They supply you with example requests with the json all right there as well as the expected responses.  
The flag up fields that are mandatory and header fields and separated so you can be aware of differences and adapt these into your test plans and  eventually your postman test collections.  They can handle authentication
as well and again if set up correctly deal with tokens etc or different types of auth for different clients within the same page. A swagger is fab training wheels for you to find your feet testing an API and once you feel comfortable you can start poking holes in it.  

## The Swagger Is Not Gospel 

As useful as the swagger is can't always be trusted however and you need to test it like anything else. I recommend if it has auth trying every call and checking for 401s : Unauthorized, once authorized try that again and check how mandatory those fields are, check the 200s 204s are coming back as expected and they handle duplicate requests for things like account creations in PUTs or POSTing the same details twice. Each Swagger should have details of the responses that you are expecting to get when you send on a request. Remember this list was built by whomever created the swagger is an is not necessarily complete.


## JSON And His Bracketnauts 

with API testing you'll probably be writing a bunch of JSON. If you haven't had much exposure to coding at this point you'll probably have the problem I had which was you'll mess up your brackets {} or miss off a comma or a [] for an array as you just aren't use to using them or you copy pasted from Notepad++ and missed a bit off. This is one of the places Swagger falls down as well, within the "try it out" boxes with the example code you can remove things by accident when adding in your test responses and it will just give you a 400: Bad Request with little to no reason as to why. It is really hard to work out where you've gone wrong and sometimes it is because you've 
copy and pasted in from a PBI/Story/item and it has added a bunch of random spaces which you can't see. I have a tip for you here. Copy paste it into Postman. Postman or VS code. Both will tell you where you've gone wrong and highlight where you need to fix things. 


## Validation And Required Fields 

Validation and Mandatory fields / boxes will be a thing you will have probably come across during your testing journey or just in you day to day with the apps you use or rely on. In my experience however they do tend to get forgotten about by developers when they knock up an API. Typically not supplying things for mandatory/required fields should give you a ticket to 400: Bad Request Ville but this is usually a great opportunity to cause some explosions and get some 500s where validation has been missed or sending something unexpected.

## HTTP Codes And Checking For Teapots 

I'm a major geek about HTTP Codes because of the API testing I've done over the years. The full list of there is here: https://developer.mozilla.org/en-US/docs/Web/HTTP/Status and I'll explain a couple that 
have brought me joy and sadness. Most of the time you will want to be getting things in the 200 range depending if data is coming back or not and depending on the kind of data that was supplied in the first place.
I haven't encountered many 300s in my API testing time but I haven't tested a massive range of APIs. the 300 range deals with redirection. The 400 range deals with client errors. This can either be caused by a lack 
of permission your side in relation to what you are sending or a lot of the time your authentication has timed out but sometimes the admin you are authenticated at doesn't have permission to do that. Other
times it is due to the Request type being wrong, you could be sending your request as a GET and it is supposed to be a POST 405: Method Not Allowed. My favourite of the 400s is 418: I'm A Teapot and 
I recommend if you are involved in building an internal REST API you encourage your development team to build in a legit 418, bonus points for custom error messages and Postman tests!

 ## The Joys of 500s And How You Should Never See Them 

This is where my HTTP code geekiness. I love getting 500s when testing APIs. I will do a little victory dance, terribly unprofessional I know. 500 known to its friends as Internal Server Error means 
you hit the API so hard it fell over and had a little cry or which I mentioned previously, you did something the developer who wrote the API didn't expect. This is QA bread and butter, these are the 
bugs/errors we live for right? I am of the mind you should NEVER see a 500 in the API you are testing regardless. I have argued this with developers it should be able to handle whatever you send and it 
if can't it should supply a 400 or an appropriate 400. They should never be created and used on purpose. 500 is just not ok which is why they make me so happy.


## Postman 🚀

I mentioned Postman briefly earlier on. When I finished started testing APIs I installed it (https://www.postman.com/downloads/) set it to darkmode and went back to the swagger as I found it too overwhelming. 
If the API you are testing is simple or you can't get on with swagger, Postman is the way to go. 
I love using Postman now and not only for how easy it makes everything but it is a great place to store little API calls you only use occasionally and a fantastic playground to set up a API test collection that you could eventually add into your pipeline. It has amazing scope for writing tests with little test snippets to help you along the way. 
 

## Mocking And Shouting BEES Beeceptor🐝

During my time API testing, other than 500s the thing that has bought me the most joy is Beeceptor https://beeceptor.com/. Similar to Mocky, Beeceptor allows you to knock up a URL Endpoint to intercept your requests and send on any custom response you want.  It doesn't require much setup and is a great way to mock a client request or help check a process beyond your API will work. I had to use this a lot for the first API I tested. It had a lot of moving parts and required notification functions to be run for to local systems. It often took me a while to set everything up and trial and error but when the notifications came through to Beeceptor and it sent on its message I couldn't help but shout BEES in glee. After months of this me and Beeceptor are firm friends, it even helped me with a rather unpleasant SOAP API process I had to debug.

## When It Gets SOAPY And Final API Thoughts

I feel unlucky as I have had to deal with SOAP. it is REST APIs shameful older brother and the less said about it the better. It has its own rules for error handling and isn't really a fan of being helpful in anyway in my experience. SOAP requests are in XML which is not much fun to write either and must easier to get wrong.

I hope some of the things I have said have been useful or at least given you a place to start with your REST API testing journey. I hope you now know a little more and most of all feel more prepared to tackle an API if a wild one appears and casts Test Me. I am by no means an expert but all experience, good or bad helps shape us and any knowledge we can pass on can be useful one way or another. 




