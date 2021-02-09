# Ask a Stupid Equestrian

So this horse trotted into a pub. 

"Why the long face?" asked the chap behind the bar. 

"I've been testing software all day," replied the horse.

"Testing software," the barman chortled, "is _easy_, you just need to make sure it does what it’s supposed to.”

The horse bridled at that and picked up three beer mats while whinnying "you can think of it this way: there's the things we need to do" and it jabbed a fetlock at the first mat, "the things we specified we would do," a point at the second, "and what we implemented," with a final poke at the third mat.

<p align="center" width="100%">
    <img width="30%" src="mackeson.jpg" alt="Mackeson beer mat"> 
    <img width="30%" src="mainzer.jpg" alt="Mainzer beer mat"> 
    <img width="30%" src="heineken.jpg" alt="Heineken beer mat"> 
</p>  

"Hmm ... drink?"

"Wine?"

"Red or white?"

"Got any Eck?"

"Eck wine?"

Silence for a moment. The horse raised its eyebrows slightly. The barman pulled his own long face and the horse turned back to the mats, arranging them into an overlapping trefoil.

"So the bit where all three intersect, that's where the novice might imagine the tester does their work: we needed it, we planned to do it, we built it, and now we just check it before we ship it."

<p align=center>
<img width="75%" src="sweet.png" alt="Highlight the intersection of Specified, Needed, and Implemented"> 
</p>

Glancing around, the barman saw there was no-one else in the place so he was saddled with the horse, but hopefully not furlong.

Barely out of the gate yet, the horse continued enthusiastically. "Checking the software against the spec could confirm some of that but it’d find mostly things that we'd said we wanted but hadn't done." 

It gestured towards the mats again, “that’s this part.”

<p align=center>
<img width="75%" src="unimplemented_spec.png" alt="Highlight the Specified but Unimplemented area"> 
</p>

"What about finding things that we _needed_ to do but didn't do, eh? We can't find all of those by checking the spec and you can bet your bottom dollar there'll be some." It waved a hoof towards the first mat and continued on "some of them we might not even _know_ we needed to do."

<p align=center>
<img width="75%" src="unfulfilled_need.png" alt="Highlight the Needed but Unimplemented area"> 
</p>

"Hmmnmmnn?" the barman said distractedly, like a blinkered project manager waiting for a break in the conversation to request another feature. 

But the horse had got the bit between its teeth now, "and then there's the things that we've implemented that no-one asked for." Nostrils flared, it stabbed the third mat. 

<p align=center>
<img width="75%" src="unexpected.png" alt="Highlight the Implemented but not Specified area"> 
</p>

"Sometimes we’re onto a winner — a bit of extra useful functionality — but we might also have inadvertently changed existing behaviour somewhere else in the product ...” 

The barman was having a mare. Still no other punters.

"... and then we might have implemented stuff that wasn’t needed; customers don't want it, or it interacts badly with something else, or ..." and it dropped its head as it gestured in the general direction of the third mat again, feeling foalish at the tears in its eyes, "... where's the manual for finding that, eh?"

<p align=center>
<img width="75%" src="undesired.png" alt="Highlight the Implemented but not Needed area"> 
</p>

"Time to rein you in, I think" said the barman, walking round to the horse and (infeasibly, but no more so than a horse speaking eloquently about testing) putting his arm round its shoulders.

"And as for stable builds ..." but from long experience the barman knew it ill behooved him to let the horse get on to that so he ushered it towards the door and turfed it out.

"'Night."

"'Neiggghhht."

## Credits
An earlier version of this story appeared in [Hiccupps](https://qahiccupps.blogspot.com/2013/08/ask-stupid-equestrian.html). It is based on Iain McCowatt's excellent article [Spec Checking and Bug Blindness](http://web.archive.org/web/20140729150250/http://exploringuncertainty.com/blog/archives/253) (linked here from the [Wayback Machine](http://web.archive.org/)) with his kind permission.

## James Thomas

James is one of the founders of [Linguamatics](https://www.linguamatics.com), the world leader in innovative natural language-based text mining. Over the years he had many roles in the company, building teams from scratch in development, tech support, and testing. Testing is where he feels at home.

James is Vice President of the Association for Software Testing, runs the Cambridge Exploratory Workshop on Testing, wrote the [Peers Exchanging Ideas](https://github.com/associationforsoftwaretesting/peer-conferences/blob/master/AST_Peer_Conference_Guide.md) guide to peer conferences, and won the EuroSTAR Best Paper prize in 2015 for [Your Testing is a Joke](https://huddle.eurostarsoftwaretesting.com/wp-content/uploads/2016/04/eBook-Download-Your-Testing-is-a-Joke.pdf).
You can find James on Twitter as [@qahiccupps](https://twitter.com/qahiccupps) and read his blog at [Hiccupps](https://qahiccupps.blogspot.com)