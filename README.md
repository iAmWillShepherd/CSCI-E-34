[Project proposal](https://github.com/iAmWillShepherd/CSCI-E-34/blob/master/README.md#project-proposal)

# Project proposal

Tl;dr

I intend to design a tool that trainers, their clients, and athletes can use to design workout programs and track program progress. There will be a web and mobile piece. The web portion will be for workout creation for trainers and athletes and client management for trainers.

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

The pleasurable state I'm focusing on for athletes is giving them the ability to see their workout progress graphically and preventing the loss of data. Notebooks are prone to be lost, especially after an intense workout, and is generally inconvenient having to carry around pen and paper to log workout progress. 

The pleasurable state I'd like clients to achieve is the ability to locate a trainer and signup without any friction.

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

The trainer app needs to make creating and sharing workouts as simple and frictionless as possible for trainers and athletes. That means that the app needs has to be flexible enough to support arbitrary workout plans: they shouldn't have to jump through hoops to switch from a paper based program to this application. The client facing part of the app needs to make finding a trainer and signing up as seamless as possible and logging workout progress needs to be simple and quick. Clients and trainers may have a pre-existing relationship, but I will focus on those that do not have a pre-existing relationship with a trainer. This means there has to be an easy way for clients to search for and signup with a trainer.


> On what sort of hardware and software will the users be using your application?

All users would use a mixture of the web and mobile. My expectation is trainers would have heavier web usage because they are managing multiple clients and building or updating workout programs.

> What sort of environment will you use for the quick prototype that this term project requires? And what sort of development environment would you use to develop this system industrially, if that’s different?

I assumed we were required to use Balsamiq. If that is no longer the case, perhaps I could use Sketch? I would likely use a basic text editor for the web app and Xamarin/Android/iOS for the mobile apps.
