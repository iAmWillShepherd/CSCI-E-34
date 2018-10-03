[Project proposal](https://github.com/iAmWillShepherd/CSCI-E-34/blob/master/README.md#project-proposal)

# Project proposal

Tl;dr

I intend to design a tool that trainers and athletes can use to design workout programs and track program progress.

### Story

A few years ago, my cousin an I were talking about personal fitness and his life as a personal trainer. At the time, I was trying to develop a new training program that would help me get into competition shape for a meet I was hoping to compete at. I asked him if he knew of any good apps that I could use to build my workout program and to track progress against the program. Prior to asking him this, I had done my due diligence and tried out over 10 fitness tracker apps across two platforms (iOS and Android). None of them solved my problem: an app that allows me to easily create workout programs and track my progress against it. He told me that he didn't know of any good apps and he described his workflow to me which I will summarize below:

1. Create a workout program on paper
2. Format the document as a worksheet
3. Bring the workout program and a notebook to the training session
4. Write down what the client did (e.g. exercise, weight, sets/reps)
5. After he's done with his clients, enter the data into Excel

As we continued our talk, I started to get the feeling that personal trainers couldn't apply their practice at scale, so I ask him what was the maximum amount of clients he felt he could take on and why. His answer basically confirmed my suspision. Since personal trainers tend to be more hands-on and time being finite (at least to us humans), they are limited in the amount of clients they can take on for the following reasons:

- Trainer and client may not be available during the same time of day
- Most clients work full-time (aka 9-5) creating extreme demand to have sessions from 4PM to 7PM
- The time demands of manually keeping each clients progress up to date

At this point, it was clear that his main problem is a scheduling problem. Like with most scheduling systems you can improve throughput by varying the time it takes to complete a task or by having more things do a task. Since we can't clone my cousin, i'll have to focus on reducing time needed to build a program.

## QA

> What sort of users will use this system?

The table below describes the users of this solution

| Persona | Description                                                  |
| ------- | ------------------------------------------------------------ |
| Trainer | A trainer is a person who designs workout programs for their clients. They need to keep track of all their clients in addition to making minor tweaks  to the program over time. |
| Client  | A client in this scenario is anyone who consumes the workout programs of a client. They are not interested in creating a plan, but they do want to see their progress over time. |
| Athlete | An athlete will design their own workout programs. They need to keep track of their personal progress in addition to making minor tweaks to the program over time. They are basically a trainer with themselves as a client. |



> What sort of business problems will the users be trying to solve, or what sort of pleasurable state will they be trying to enter and maintain?

The business problem that has the biggest impact to a trainer's bottom line is client count, which is constrained by time. My hypothesis is that decreasing the amount of time spent managing client progress will increase the number of clients a trainer can take on.

The problem I will focus on for athletes is loss of data. Notebooks are prone to be lost, especially after an intense workout, and is generally inconvenient having to carry around pen and paper  to log workout progress.



> What would your users consider to be the characteristics of a good solution, or of a good pleasurable state?

1. Creating and sharing a workout program is **seamless** - Since I am trying to solve for time, the experience of creating a program and getting it out to clients has to be less painful than the status quo
2. Tracking progress is **simple AF** - Gyms can be busy environment and workout can often include a time component, so any good solution must support quickly logging progress too avoid derailing the workout.
3. Limited amount of required data entry - Workouts are typically pretty repetive so there is ample oppurtunity to off-load some amount of data entry.



> What is the expected (hoped for) size of the user population? What is the expected frequency and duration of sessions per user?

The expected number of people who will use the app initially can be counted on two hands. Of the folks who use the app, one will be a trainer, I'd expect him to use it during his training sessions throughout the day. In case you like numbers :smile:

| Persona | Expected | Hoped for :crossed_fingers:       |
| ------- | -------- | --------------------------------- |
| Trainer | 2        | All resistance trainers/coaches   |
| Athlete | 5        | All people who want to train      |
| Client  | 2        | All people who want to be trained |

_All = % of world population, with a phone and access to the internet, and wants to train_

Each interaction with the app is likely to be less than 30 second unless the app is being used with a timed workout. Non-trainers would mostly use the app during their workouts, so it will not be an integral part of their lives, nor do I expect it to be.



> Provide some description of the economics of the system. For example, is your project an app or service that are selling? If so what and for how much and to whom? Are you trying to enable/improve user productivity or decrease error rate? If so, how, for whom, and some notion of the cost of user time and errors.

This project would be have a mobile and web component. If I do build it, I'd likely do it in the open. I don't know if anyone is willing to pay for this, but I'll keep my option open :smirk:

I'm trying to improve efficiency for trainers by removing as much manual data entry as possible and automating away their most repetive tasks. I'm trying to decrease error rate for non-trainers by removing  paper from the equation (maybe a better idea is GPS-enabled notebooks?) which can improve efficiency by removing the need to manual log sets.



> Tell me about the competitive landscape in your app’s market, and how yours will be better. What is your user's best alternative to using your app?

There are a lot of fitness tracker apps, none of the ones I've played with make it easy to create a workout program for yourself or others.

The best alternative I know of is a mixture of excel, paper, text-messages, and one of the general purpose tracking apps (for logging workout progress).

Most of the applications in this space deal with the business side of running a PT business such as, scheduling, marketing, promoting, etc. This application will focus on the value generation part of a trainer's job.



> Write a paragraph or two discussing what you consider to be the essence of your project’s UX needs.

The trainer app needs to make creating and sharing workouts as simple and frictionless as possible. That means that the app needs has to be flexible enough to support arbitrary workout plans: trainers shouldn't have to jump through hoops to switch from a paper based program to this application. The client facing part of the app needs to make logging workout progress as quick as possible. So, the essence of my project's UX needs is ease of workout program creation and speed of logging workout progress.



> On what sort of hardware and software will the users be using your application?

All users would use a mixture of the web and mobile. My expectation is trainers would have heavier web usage because they are managing multiple clients and building or updating workout programs.



> What sort of environment will you use for the quick prototype that this term project requires? And what sort of development environment would you use to develop this system industrially, if that’s different?

I assumed we were required to use Balsamiq. If that is no longer the case, perhaps I could use Sketch? I would likely use a basic text editor for the web app and Xamarin/Android/iOS for the mobile apps.

# User Stories

1. Charlie quickly sees the details for the last time he did that exercise.
2. Charlie is in the middle of his workout and can easily log his progress.
3. Nola pulls out her phone to start a workout and doesn't have to click through a bunch of options to start that day's workout.

> Charlie quickly sees the details for the last time he did that exercise.

Charlie is brought out of a trance state by his phone ringing. He looks down and sees it’s from his soon-to-be wife. It’s tax season, and he’s juggling night-school, work, and wedding planning. Work has kept him stressed for sure, he spent the day auditing his company’s finances. The _boss_ just told him he better get his share of the chores done tonight. He looks up, “shit, I ’ma be late,” it’s 5:34! He intended to get to the gym by 6:00 so he could be home by 9:00. With Houston traffic, he’d be lucky to make it by 6 even he teleported himself to his car.

He rushes into the gym at 6:08. not bad! After hurriedly changing, he heads over to the bench. It’s International Chest Day. “FFFFFFF***!” (if you know you know 🤣) He forgot what he did last week. But no worries! He remembers that app he’s been using for the past few days. He opens the app, and it immediately pops up with ~a gif of terry crews flipping his pecs~ the day's workout. The app knows it’s Monday and it has the two pieces of info he needs in his life: what he did last time he did this exercise and an overview of what he has to do today. He’s supposed to increase his weight to 85% of his 3rm. He loads up 285lbs and does his first set. Invigorated by the app saving the day, he opens it up to log his set. He’s delighted by the sheer simplicity of it. The app just asked if he was able to complete the set: he selected yes.

> Nola pulls out her phone to start a workout and doesn't have to click through a bunch of options to start that day's workout.

Nola looks around the room at her teammates doing epic fist pumps after successfully shipping a significant redesign of her company’s most popular product. She’s had a hell of a day. Her team is full of cowboys. They often wait until the last possible minute to get Q.A. involved. She’s spent the past 3 days doing manual testing for the new features they are shipping. No one thought to bring her into the process sooner, so she could have drafted test plans and automated the new tests. Oh well, it’s done now. Stressed out, she tells her team she’s dipping out. The gym is beckoning.

She walks in the gym and gets changed into the proper gym attire. It’s leg day, so she heads to the turf to do some active stretching and mobility work. Her pre-workout is kicking in, and she’s ready to hit the rack. She pulls out her phone so she can see what weight she’s working with today. After opening the app, she grins. The app knew it was her leg day and presented her with the option to start the day's workout. She came to the gym to reduce stress, not add to it by having to tap a bunch of times just to start her workout. Pumped by the caffeine and respite from work, she gears up and bangs out a solid warm-up set of 12. she pulls out her phone and sees an option to add her completed set as a warm-up. She loves data and is hoping to see if her hypothesis about warm-up sets is correct, so she’s been logging all her warm-up sets. So far she’s been pleased with how flexible it’s been. She often warms-up until she’s feeling good enough to get into her working sets.

> Charlie is in the middle of his workout and can easily log his progress.

Charlie is headed to the Apple store to have their geniuses migrate data from his 2015 MacBookPro onto his new 2018 MacBookPro that cost more than some people’s income. He’d typically do stuff like this on his own, but lately, Apple has been making it too complicated with their dongles. He feels his wrist buzz. _Reminder: GYM_. “Oh yeah, I need to get a case!”. He grabs a case for his new iPhone so he can track his workout without damaging it.

As he’s warming up on the Stair Master™, he’s checking out what today’s workout entails. HIT and agility work. His wrist pulses again, _Goal reached!_ Time to head out to the turf. After opening the app, he quickly taps the option to start the workout and waits for the stopwatch to signify the start of the workout. After his first interval. He opens the app. _Did you complete the interval?_ Today was tough; he has to be honest with himself and say no. Now he gets to input how much of it he completed quickly. His wrist buzzes. _30 seconds to next interval..._ He puts his phone down and get’s ready for the next round.
