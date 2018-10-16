---
layout: post
title: Challenges when doing remote pair programming and how to overcome them
tags: [eXtreme programming, DevOps practices]
---

Known not only as one of the 12 practices of [eXtreme programming](https://ronjeffries.com/xprog/what-is-extreme-programming/),
but also as one of the DevOps practices, pair programming is a technique that becomes more and more popular every day.

Doing pair programming doesn't sound difficult, but this doesn't mean there are no challenges to face in order to feel its benefits.
There are challenges, especially if we try to apply this practice remotely when working in distributed teams.

<!--- excerpt -->

## What is pair programming?

Pair programming can be shortly described as two programmers working together to solve a task, using a single computer. 

> *Wait! Four hands and only one keyboard?*

Not four hands, but two roles:
* **driver** - the person that actually writes the code
* **navigator** - the person that observes the driver and reviews the code as it is being written 

> *Wait! So two programmers are doing the same task? This sounds rather inefficient!*

Don't fall into this trap! Give it time to see its benefits! It may be that at first a pair finishes the task almost in 
the same time a single programmers does. But the code quality is undoubtedly better. As time passes, you will
notice that the **knowledge sharing inside the team is done quicker** than before applying pair programming.

> *So two heads really are better than one!*

Yes! Working in pair, you will have **the code reviewed by two programmers**, a task that was implemented having a **better 
design**, a **better code quality** and that was **better tested** than it would have been if it was implemented by a single programmer.


## How to successfully overcome challenges in remote pair programming

I am working in a company that embraces extreme programming as one of its values, so pair programming is a globally
applied practice in my division and project. Since last year, we have started working as two distributed teams and even
if we were fans of doing pair programming, we were all asking ourselves how this will work when the driver and the navigator
are working remotely.

After doing this for one year, I can now write down a list of challenges that we faced during the process.

### 1. Find a suitable tool for remote desktop control

If you start doing remote pair programming, you will want to be able to switch the driver-navigator roles as easy as possible.
If the pair was collocated, this switch would mean just passing the keyboard around.

Luckily, [TeamViewer](https://www.teamviewer.com/) is a great tool for remote desktop control. You can use it to connect
to a remote desktop, see the remote screen(s) and take over the mouse and keyboard control whenever you want.

### 2. Find a lightweight tool to always keep in touch to your pair

Even if TeamViewer is smart enough to offer you sound/video features to keep in touch to your pair during the process,  
personally I didn't have a such a great experience using its audio features on my Linux machine, so I dropped it
and kept using it only for remote control.

The commonly agreed choice in my team was using the Slack calls. We were already using [Slack](https://slack.com) for
team communication, so we happily gave the Slack calls a try when this feature was released. And we didn't regret it.

### 3. Find a suitable way to do a remote architecture design

Maybe not all tasks require having a complex architecture design before starting writing code, but there will always be 
some that do. In such situation you will want a tool to easily draw some components, class diagrams, and the interactions between them.

draw.io is a good choice for this, but it can be a burden when all you want is maybe a quick draft to explain an idea to your pair. 

So, depending on the context, carefully choose your weapon!
* [draw.io](https://www.draw.io) helps you to draw clear, proficient diagrams of your system.
* [Sketchpad](https://sketch.io) helps you to sketch your idea on the spot.

### 4. Adjust to timezones

This can be a real challenge if the pair members are from different countries and implicitly there are time zone differences.

For example, there is a mix between Romanian and Belgium developers in my current team. Because Belgium is one hour ahead of Romania,
some of us will always arrive at work one hour earlier than the remote ones, or will leave one hour earlier in the evening.
There can be a desynchronization when it comes about lunch time as well. Working in different offices, you can have
different meetings too, so yet another moment when you'll have to leave your pair alone.

The important point here is to be aware that this will definitely be on your table when it comes about remote pair
programming and how to deal with it.

And because pair programming is about knowledge transfer, having the pair split for
1-2 hours a day is not that harmful. Just take care to commit your changes to version control when you leave your
computer and your pair can take over for the next hour. You'll sync when you're back. If your pair calls it the day before you,
make sure you leave him/her a message about what you continued to do in his/her absence.

### 5. Don't forget having breaks

Because you are pairing with a remote colleague and you cannot take a break (and maybe walk and talk together), 
this doesn't mean you shouldn't have it separately. Pay attention at this aspect and don't fall in the trap of sitting
in front of the computer all day long. Apart from being recommended, a break can refresh you thoughts and give you a fresh
grasp of what you are working on.

So, don't be shy and ask you pair to have a 5-10 min break at every 1-2 hours. Take your headset off, walk around,
watch the sky, do some casual chatting with your co-located colleagues.

### 6. Re-pair

Working remotely can make the re-pairing even more difficult. Step out of your comfort zone and try re-pair at least every 2 days.

Yes, the story lead will have to do a handover to his/her new pair, but think to how fast the knowledge transfer is done by re-pairing.
If your story is not done in 2 days, then your pair can easily pick up the next story of that epic and be the lead of it.
He/She will pair up with someone else and instead of being only 2 that know about that specific topic, in only 3 days, you will be 4.

Just find what's the time interval that best fits everyone to re-pair. If a day feels too soon, try not spending more than 2 days with your pair.
Start passing your knowledge to a third person as quickly as possible!

### 7. Be ready for some remote chatting

It's practically impossible to work 100% of your time. We write software that has to be tested and deployed. The last two activities
imply mostly staying, observing and monitoring a CI/CD tool in action. Use this time to do some cultural exchange with your remote pair.

If you want to have a successful distributed team, get to know your remote colleagues as if they would work in the same office as you.
Find out their hobbies, food, believes, routines, opinions and be ready to be surprised on the cultural differences (or similarities).

Cross the distance barriers and start winning friends!   

### 8. Get a comfortable audio headset

Remote pair programming implies spending a lot of time with a headset on your ears. Take some time and get one that
doesn't give you any head or ear aches. You want to feel as comfortable as possible and put all your focus on pair
programming. 

And don't forget to share them with your team! You are all trying your best to make remote pair programming work,
so if you felt the pain of your audio headset, most probably your colleagues would do as well.  
 
### 9. Don't forget to interact with your co-located colleagues

If you have more remote colleagues than co-located, there is a higher probability of doing remote pair programming. 
This can affect your relationships with your peer colleagues. If you are lucky, you will have lunch together. 
Otherwise, there is a risk to be days when you don't talk at all.

Take care of the interactions with your colleagues. Make a habit of having lunch together, or taking 1-2 breaks all at
the same time to change ideas, chat, align.

Fight the routine! Don't let walls to grow between you!


## Summary 

I think that we can all agree on the fact that doing remote pair programming is not going to be easy in the first weeks
(maybe even months), but the attitude towards making it work is what matters the most. Making the people believe in it, 
being open minded when facing its challenges and putting all the good will and effort to make it work are only a few of
the steps to be successful in remote pair programming.

When we 'migrated' from doing pair programming in our co-located team to doing it remotely, I often heard in my team the following words: 
> It's not about bad tooling, it's about team's attitude. It's about if your team really wants remote pair programming!

Yes, you can blame the distance or the bad tooling that make your job difficult, but if you are in a team where everyone
wants to be good at remote pair programming, you have no excuses. Every pain can be fixed. Nobody says it's gonna be easy,
but in the end it will definitely worth the effort!