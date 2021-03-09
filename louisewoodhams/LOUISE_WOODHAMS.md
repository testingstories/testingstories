# Swagger Like Jagger - An API Testing Story By Louise Woodhams

## APIS - Those Are Things 

When I started testing REST APIs I have no idea what they were and for a fair chunk of that time I wouldn't have been able to give you a decent definition.  
They are a middle man to me and the API I was primarily testing was built to sit between a system I knew very well and an external client system.  
It acted in a bunch of ways like a translator so I tried to translate it into something I understood.  

## Context Is King 

This is how I managed to test this API without really understanding why it was a thing. As a tester I find context vital and if I can find a way to relate the unknown scary thing to something I've tested or experienced before it becomes more manageable. I am usually terrible at asking questions but for this project I asked for context and it really helped. I kept drawing on the system I already knew and investigated the client configuration that would be used with this API to build true to life testing scenarios. This actually found some decent bugs and some holes in the UNIT testing.  


## Swagger Training Wheels 

The development team had thankfully added a swagger to the API I was interacting with. I love a swagger. It is a great place to start with API testing. If it is built right (ill go into this more later) you can gain an understanding pretty quick, consider a bunch of test cases in advance and actually import it into a postman collection which with some tweaks is usable from the get go. 
Swaggers are colourful. I think these colours helped me learn and retain REST APIs quicker.  They supply you with example requests with the json all right there as well as the expected responses.  
The flag up fields that are mandatory and header fields and separated so you can be aware of differences and adapt these into your test plans and  eventually your postman test collections.  They can handle authentication as well and again if set up correctly deal with tokens etc or different types of auth for different clients within the same page. A swagger is fab training wheels for you to find your feet testing an API and once you feel comfortable you can start poking holes in it.  

## The Swagger Is Not Gospel 

As useful as the swagger is can't always be trusted however and you need to test it like anything else. I recommend if it has auth trying every call and checking for 401s, once authorized try that again and check how mandatory those fields are, check the 200s 204s are coming back as expected, they handle duplicate requests.  

 

## Json And His Bracketnauts 

## HTTP Codes And Checking For Teapots 
https://developer.mozilla.org/en-US/docs/Web/HTTP/Status

## The Joys of 500s And How You Should Never See Them 

## Validation And Required Fields 

Validation and Mandatory fields / boxes will be a thing you will have probably come across during your testing journey or just in you day to day with the apps you use or rely on. 
 


## How To Visualise Without The UI 

## Tools and Friends 

### Postman 🚀
I mentioned Postman briefly earlier on. When I finished started testing APIs I installed it (https://www.postman.com/downloads/) set it to darkmode and went back to the swagger as I found it too overwhelming. Now I love using Postman and not only for 
 

### Mocking With Beeceptor🐝

 https://beeceptor.com/



Format 