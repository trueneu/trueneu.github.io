# Tutorials considered harmful

Disclaimer: everything below is just my opinion. I’m an engineer with about 10 years of experience, I worked for small shops, medium-sized firms and large corporations, communicated with a lot of people and read a countless number of articles on tech. Below is my view on a particular aspect I run into on daily basis, whether reading or talking to people. I might be totally wrong, and if you want to discuss it, let's do so in the comments section.

First of all, let’s establish some well-known facts about learning and acquiring knowledge.

# Learning

![https://xkcd.com/749/](https://imgs.xkcd.com/comics/study.png)
<figcaption><a href="https://xkcd.com/749/">https://xkcd.com/749/</a></figcaption>

One of the qualities defining Homo Sapiens is curiosity. Essentially, being curious equals being hungry for knowledge. Now, any living organism is interacting with environment in some way, and one can define curiosity as a mere 'will to live'. Those who didn't adapt to changing environment well and fast enough, are extinct, and were not curious enough. Those who did, were curious, were striving, were successful and thus prosper. But I mean something a bit more specific: curiosity is the interest in how things work as opposed to just using things. Dive deep, if I may.

Little children feed their curiousity by tearing apart dolls and toy cars to look what's inside. It's especially interesting if a toy has a lot of moving parts: a child comes up with certain assumptions how pieces fall together, builds a hypothesis and may try to prove or disprove it. Let's take this part out and re-assemble the car without it, will my car still run?

In a sense, that's what we're doing in our professional lives every day (except our objects aren't toys). We disassemble - in a broad sense - stuff, reassemble it in different order, poke bits and bytes with a stick, play around with different systems and read source code to get a better understanding how things work under the hood. We do that to be able to use things more effectively, and to feed our natural curiosity. IT as a field is great for this type of hunger: the amount of information is so vast that there's enough for a bunch of peoples lifetimes.

There's another way of gaining knowledge without necessarily having to experiment yourself, namely formal education. You have teachers, or professors, which are - at least, supposedly - masters of their fields. They present the information in a well-structured, systematic way, starting from fundamental, basic and simple knowledge, all the way up to highly complicated and often abstract concepts. The media can differ: lectures, books, VOD courses, webinars, etc. Although you can't exactly call it 'formal' if you're not supervised by a trained teacher, I'd still very much consider it 'education' if you're reading a book written by that teacher.

# Fundamental Knowledge Importance

My humble opinion is our industry as a whole took a wrong turn sometime in the 90s. It's been worsening year after year ever since, and there's seemingly no end to it. What am I talking about? Let me give you an analogy.

OK, so imagine a surgeon. This particular surgeon has worked for certain hospitals throughout her career. She has a nice resume, soft-skills and hard-skills, years of experience and overall, a good record and a good salary. But there's a problem.

She doesn't know how the human body works as a whole. See, she's a knee surgeon. She knows everything about knees. She has seen thousands of different knees of different sizes, shapes and ages. If you have a knee problem, there's no one that can treat you better. But here's a catch: if during a surgery something else goes wrong, say your heart starts to give in all of sudden, or your lungs malfunction, or a blood knot gets into the bloodstream... You're toast. She doesn't know what to do in these types of situations, and she'll desperately need help from another doctor. But under the time constraints, chances are when the help arrives, it's time to call it. Sorry. She's just a knee surgeon.

![](tutorials-harmful/therac-machine.jpg)

_Medical equipment actually kills people from time to time_

Does it sound absurd to you? If it doesn't, it should. This is the kind of the vibe I get from the absolute majority of developers nowadays. Sure, they know their knees - a language, a framework, an API - and they've probably mastered that particular tool. But they have no idea how the body - the environment around - works. Just the basics would be enough. But a lot of people have no clue how the CPU works, or how scheduling works, or what's a process state, or what's a process even, or how virtual memory works, or a filesystem, or dozen of other things they actually use every day in their professional lives. I mean, you don't have to know how a car works to drive it, but we're kind of car mechanics here. Things go wrong every day, and we have to debug and troubleshoot stuff every day, and the better we understand the ins and outs, the better we can diagnose the problem, the better we can follow it up so it never resurfaces again. Without understanding, our fixes are merely band-aids. They help now, but in a week or two they're gonna be obsolete. And the wound will bleed even worse, because computers don't self-heal.

# Tutorials

![https://xkcd.com/744/](https://imgs.xkcd.com/comics/walkthrough.png)
<figcaption><a href="https://xkcd.com/744/">https://xkcd.com/744/</a></figcaption>

A large portion of content one can find on the web about information technologies is tutorials. Usually, a step-by-step list on how to achieve this particular thing, without digging too deep into details, or explaining the rationale behind steps taken. More often than not, tutorials are written in a specific way with a lot of assumptions, for example that everything else around is set to default. More often than not, tutorials are written by people that just have achieved something themselves, and are eager to share their knowledge with the world.

While inherently sharing knowledge is a good thing, and I can't not support it, I'm questioning the whole idea. The quality of the information in this case is often sub-par. The reason is that the person has just learned something herself: she didn't put enough time in to truly understand it, to experiment with it, to try 9 more different approaches and come to the conclusion that the 7th is the best. There's no attention to details, as the person is not aware there are details. It reminds me of Dunning-Kruger effect: the less you know about something, the more likely you are to be victim to the cognitive bias of overestimating your knowledge. It's not necessarily because you're intentionally ignorant: you just don't know any better, at least yet.

This creates the soil for such incomplete knowledge adoption. It's one thing to write a tutorial, but if it's taken as a Holy Grail by readers... Oh boy. System administrators in ex-USSR countries had this joke about 10-15 years ago: there's this site with a great amount of tutorials on FreeBSD, lissyara.su. There was a generation of young sysadmins using the site as a bible, and not having read anything else. As a result, the moment they encountered something not covered in tutorials, they were completely stuck. So when a person demonstrated a lot of practical skills without any fundamental knowledge whatsoever, people would call him a "lissyara adept", or just "lissyara", in a diminishing way. Without understanding how things work, you can't repair anything. It's like giving crutches right away instead of treating the fracture.

There's a reason why a professor usually has years of experience in the field, ideally she has her own course and own textbook and own set of assignments. She knows the subject in and out, so she can, based on knowledge and experience, tell important from unimportant, structure the information in a digestable way, and pitch it right. Most tutorial authors don't have any of that. Why would they? They've learned the concept a day ago themselves! They're just translating stuff as is, there's no capability to restructure it or rethink it or tell it from a different point of view. If there are factual errors, or some important detail is omitted, or the article is plain wrong - the author just doesn't know that. So the author translates erroneous knowledge further... multiplying and amplifying it.

And that's why I consider writing, and especially reading, tutorials harmful.

# A Way Out?

![https://xkcd.com/1760/](https://imgs.xkcd.com/comics/tv_problems.png)
<figcaption><a href="https://xkcd.com/1760/">https://xkcd.com/1760/</a></figcaption>

Fundamental knowledge is king. Sure, tear apart the toy car and try to reason about what the insides do, but don't post a "that's how you do it" article right after that. Make a hypothesis, try to prove it or disprove it, and fact-check in a more formal, theoretical form: read a book, listen to a university course, or talk to a known professional engineer, to ensure that your understanding conforms with reality. Get more knowledge on the topic, on the adjacent subjects. Better to do all of the above. Maybe a couple of times. Foster your inner child and its natural curiousity! And feed it, feed it until you're sick, and then feed it more.

It should be fun to go "oh, so that's why CPUs have protected mode and real mode!", "oh, so that's how a bootloader works!", "oh, so that's how Load Average is computed!", "oh, that's why I can't utilize my network bandwidth!", "oh, that's how JS layouts memory!" and so on. And once you get that, inside and out, that's a good article stuff. And go out there and share and write it, because the web is lacking high quality materials.

Santayana said "Those who cannot learn from history are doomed to repeat it". This applies surprisingly well to a lot of aspects of life. And no one will ever be able to learn absolutely everything. But something is better than nothing.

In the end, you probably don't want to be that surgeon that teaches their students about knees, only to find out 20 years later that the death toll was way too high because students couldn't tell liver from bladder. Or a battery from an engine. Or running from uninterruptible. Or page in from page out. Well, you get the idea.
