# A Taxing Situation

## How the UK poll tax led to a career in software testing.

Wikipedia describes The Community Charge commonly known as the poll tax as “a system of taxation introduced by Margaret Thatcher's government in replacement of domestic rates in Scotland from 1989, prior to its introduction in England and Wales from 1990. It provided for a single flat-rate per-capita tax on every adult, at a rate set by the local authority. The charge was replaced by Council Tax in 1993, two years after its abolition was announced.”  Its introduction led to riots, punk rock songs, the fall of the one of the UKs most successful Prime Ministers and my move into Software Testing.

I had accepted a job with British Telecom (BT) as a test manager on a poll tax system for 14 local authorities. At that time there were only two telecom companies in the UK. The largest BT, was contracted to provide a system to package and print the poll tax bills, payment books and ancillary documents that local authorities sent out each year. The system also printed the individual Local Authorities coats of arms on the documents. This project had started in the previous October. It was running late and the documents had to be produced before the beginning of April. I and my six colleagues had to get the project back on track. To this end we worked the extended hours expected nowadays from a Start-up.  

One night I was in the office with a young colleague from the logo design team, correcting any of the flaws in the coats of arms that were caused due to scanning imperfections. I looked up and noticed that his shoulders had slumped and he had his head in his hands. I went over to check everything was okay and he was as white as a sheet. He told me that while working on the coat of arms for the 14th local authority he had accidentally deleted those that had been successfully created for other 13. I asked him if there was a backup, to which he replied no. 

1990 was sometime before the internet was useful for troubleshooting this type of problem, so as was my habit I referred to my personal engineering notes that I had kept since 1968. Here I found that a process existed within Norton Utilities for retrieving deleted files. As luck would have it, there was a copy of Norton on site. We retrieved all of the data in about three hours.

In early March 1990 we moved the entire operation from Brighton to Woking where BT had a major printing, sorting and distribution centre. Towards the end of March we were ready to receive and process the local authorities’ data. This process involved printing each local authorities bills, direct debit instructions and payment books together with the supporting documents.

In the distribution centre were four high speed laser printers that worked at 180 A4 pages per minute. Payment books were guillotined, stapled and assembled ready to go into the hoppers of the collating machines. These machines assembled the documents for an individual, enveloped them and sorted the envelopes into walking order for the postman. 

As you can appreciate this process in itself took a considerable time but it was further extended by the 20 hours spent processing data supplied by individual authorities. We finally produced the data by the 6th of April, which was just about acceptable. At the end of this phase of the project we held a postmortem identifying the successes and weaknesses that we had encountered, one of which was the inordinate processing time of the data that we received from the local authorities.

One of the areas which we discussed at length was the processing time it took from receiving the data to creating the print files. The programming manager was adamant that it was impossible to speed up the process. In June of 1990 the programming manager left the project and the programming department became the responsibility of the systems manager. 

I was paired with a programmer to troubleshoot and correct faults that we found during testing. I took the opportunity of going through the code and noticed that the block size was only 1024 characters and each record was just over 900 characters which meant that only one record was read on each read. From my operations background I knew that any mechanical process was significantly slower than a logical process so rather than just go off my instinct I arranged a trip to Berkshire County Councils computer facility where we rented time on their large computer. 

There I saw the magnetic tapes we received from the local authorities were visibly inching forward and the discs that the data was transferring to were shaking due to the massive amount of disc head movement. Talking to Berkshire operations manager I learned that he was very concerned about the movement of the disc drive cabinets. He said “it was as if they were trying to walk across the computer room floor “. 

When I got back to Woking I discussed with my programmer what was required in order to change the block size to its maximum 32768 which would allow us to read and write the maximum number of records possible. I then contacted the ops manager at Berkshire to cost the amendment to the file block size on the disc’s. The quote was £800. I ran the costing by the systems manager and product director and we all agreed that this would be a significant performance enhancement. It took one day to amend the programs and Berkshire completed their changes on the same day.We performed some comparisons tests and the results appeared very favourable, reducing the time it took to run through the full system from over 20 hours to under 5. When the 1991 New Year poll tax took place we saved over 2010 hours in the processing time, which at the time we paid Berkshire £120 per hour making a cost saving in access of £25,000.

I am retired now and if I were to give advice to someone in today's software testing industry, it would be to: "Use notes, memories and experience  to help others correcting faults. A testers role is to ensure that  the product is  fit for purpose."

## Biography David Symonds
I joined Exide Battery computer operations as a trainee operator in 1968. Over the next 9 years I moved up the ladder to Chief Operator then into programming and systems. In 1979 I moved to Southend as a Senior Systems Analyst. Two years later I transferred to the adjoining council of Rochford as Deputy Director of Computer Services. I held this position for eight years until the department was outsourced. I was then faced with either joining the outsourcing company or being made redundant. I chose redundancy as I had been thinking about working for myself for a while. My dilemma became which area of I.T. I should specialise in. This was resolved when I was invited by International Computer Limited (ICL) to deliver a disaster recovery project as the project manager. January the following year in 1990 I accepted a job with British Telecom (BT) as a Test Manager. 

## Technical note
The large computer was a ICL ME29 mini computer made in 1979 in the United Kingdom by International Computers Limited. The disk cabinet housed a removable disk unit composed of 5 separated metal plates about 70 centimeters in diameter. A disk head worked at top and bottom of each plate. The heads moved in and out at the same time. A similar mechanism is still used today.

## Resources
- [ Poll Tax ](https://en.wikipedia.org/wiki/Poll_tax_(Great_Britain))
- [ ICL ME29 mini computer ](http://www.computermuseum.org.uk/machines/icl_me29.html)

