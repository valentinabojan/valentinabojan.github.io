---
layout: post
title: Challenges when doing remote pair programming and how to overcome them
tags: [eXtreme programming, DevOps practices]
---

Known not only as one of the 12 practices of [Extreme programmin](https://ronjeffries.com/xprog/what-is-extreme-programming/),
but also as one of the DevOps practices that increases the quality of every development team work, pair programming is a technique 
that becomes more and more popular every day.

Doing pair programming doesn't sound difficult, but this doesn't mean there are no challenges to face in order to feel its benefits.
There are challenges, especially if we try to apply this practice remotely when working in distributed teams.

<!--- excerpt -->

## What is pair programming?

Pair programming can be shortly described as two programmers working together to solve a task, using a single computer. 

> *Wait! Four hands and only one keyboard?*

I know this can sound wrong for some of you, but when doing pair programming, we have roles that we have to take care 
to switch rather often, as following:
* **driver** - the person that actually writes the code
* **navigator** - the person that observes the driver and reviews the code as it is being written 

> *Wait! So two programmers are doing the same task? This sounds rather inefficient!*

Don't fall into this trap! Give it time to see its benefits! It may be that at first a pair finishes the task almost in 
the same time a single programmers does. But the code quality is undoubtedly better.

> *So two heads really are better than one!*

Yes! Working in pair, you will have the code reviewed by two programmers, a task that was implemented having a **better 
design**, a **better code quality** and that was **better tested** than it would have been if it was implemented by a single programmer.

As I mentioned earlier, the benefits will not appear immediately. As time passes, you will
notice that the **knowledge sharing inside the team is done quicker** than before applying pair programming.
Instead of asking around when you don't know certain areas from your project, start pairing with someone that does.
After one or two days of pair programming, instead of lacking information, you will be the one able to share information to someone else.

This practice can be **perfect to ramp-up new colleagues on the project** or to **help juniors to grow faster** by learning
from more experienced developers. This way they can see how you do things on your project and can also try out by 
themselves under your guidance and observation. Of course, the more experienced developer should pay attention all the time 
on how he shares his knowledge so that the pair programming doesn't become a mentorship instead.

By applying this practice, they will become more valuable to the team and to the company in a shorter time.



## How to successfully face challenges in remote pair programming

I am working in a company that embraces extreme programming as one of its values, so pair programming is a globally
applied practice in my division and project. Since last year, we have started working as two distributed teams and even
if we were fans of doing pair programming, we were all asking ourselves how this will work when the driver and the navigator
are working remotely.

After doing this for one years, I can now write down a list of challenges that we faces during the process.

### 1. Find a suitable tool for remote desktop control

If you start doing remote pair programming, you will want to be able to switch the driver-navigator roles as easily as possible.
If the pair was collocated, this switch would mean just passing the keyboard around.

Luckily, [TeamViewer](https://www.teamviewer.com/) is a great tool for remote desktop control. You can use it to connect
to a remote desktop, see the remote screen(s) and take over the mouse and keyboard control whenever you want. TeamViewer
is smart enough to offer you sound/video features to hear/see your remote pair.

### 2. Find a lightweight tool to always keep in touch to your pair

As I mentioned in the previous section, you can always TeamViewer to keep in touch to your pair during the process. 

Personally I didn't have a such a great experience using TeamViewer audio features on y Linux machine, so I dropped it
and kept using it only for remote control. The commonly agreed choice in my team was using the Slack calls.
We were already using [Slack](https://slack.com) for team communication, so we happily gave the Slack calls a try when this feature was released.
And we didn't regret it.

### 3. Adjust to timezones

This can be a real challenge if the pair members are from different countries and implicitelly there are time zone differences.
For example, there is a mix between Romanian and Belgium developers in my current team. Because Belgium is one hour ahead of Romania,
some of us will always arrive at work one hour earlier then the remote ones, or will leave one hour earlier in the evening.
There can be a desynchronization when it comes about lunch break as well. Working in different offices, you can have
different meetings, too, so yet another moment when you'll have to leave your pair alone.

The important point here is to be aware that this will definitely be on your table when it comes about remote pair
programming and how to deal with it. And because pair programming is about knowledge transfer, having the pair split for
1-2 hours a day is not that harmful. Just take care to commit your changes to version control when you left your
computer and your pair can take over for the next hour. You'll sync when you're back. If your pair calls the day before you,
make sure you leave him/her a message about what you continued to do in his/her absence.

### 4. Don't forget having breaks

Because you are pairing with a remote colleague and you cannot have a break (and maybe walk and talk together), 
this doesn't mean you shouldn't have it separately. Pay attention at this aspect and don't fall in the trap of sitting
in front of the computer all day long. Apart from being recommended, a break can fresh you thoughts and give you a fresh
grasp of what you are working on. So, don't be shy and ask you pair to have a 5-10 min break at every 1-2 hours. Walk around,
watch the sky, do some casual chatting with your co-located colleagues.

### 5. Find a suitable way to do a remote architecture design

Maybe not all tasks require having a complex architecture design before starting writing code, but there will always be 
some that do. In such situation you will want a tool to easily draw some components, class diagrams, and the interactions between them.
draw.io is a good choice for this, but it can be a burden when all you want is maybe a quick draft to explain an idea to your pair. 

So, carefully choose your weapon depending on the context!
* [draw.io](https://www.draw.io) helps you to draw clear, proficient diagrams of your system.
* [Sketchpad](https://sketch.io) helps you to sketch your idea on the spot.
 
### 6. Repair

Working remotely can make the repairing even more difficult. Step out of your comfort zone and try repair at least after 2 days.
Yes, the story lead will have to do a handover to his/her new pair, but think to how fast the knowledge transfer is done by repairing.
If your story is not done in 2 days, then your pair can easily pick up the next story of that epic and be the lead of it.
He/She will pair up with someone else and instead of being only 2 that know about that specific topic, in only 3 days, you will be 4.

Just find what's the time interval that best fit everyone to repair. If a day feels too soon, try not spending more than 2 days with your pair.
Start passing you knowledge to a third person.

### 7. Be ready for some remote chatting

It's practically impossible to work 100% of your time. We write software that has to be tested and deployed. The last two activities
imply time to mostly stay, observe and monitor a CI/CD tool in action. Use this time to do some cultural exchange with your remote pair.

If you want to have a successful distributed team, get to know your remote colleagues as if they would work in the same office as you.
Find out their hobbies, food, believes, routines, opinions and be ready to be surprised on the cultural differences.
Cross the distance barriers and start winning friends!   


 

