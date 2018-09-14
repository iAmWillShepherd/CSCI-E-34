# Project Proposal

Tl;dr 

I intend to design a tool that trainers and athletes can use to design workout programs and track program progress.

### Story time

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

At this point, it was clear that his main problem is a scheduling problem. Like with most scheduling systems you can improve throughput by varying the time it takes to complete a task or by having more things do a task. We can't clone my cousin, so that leaves only one thing to change. 

### Users

The table below describes the users of this solution 

| Persona | Description                                                  |
| ------- | ------------------------------------------------------------ |
| Trainer | A trainer is a person who designs workout programs for their clients. They need to keep track of all their clients in addition to making minor tweaks  to the program over time. |
| Client  | A client in this scenario is anyone who consumes the workout programs of a client. They are not interested in creating a plan, but they do want to see their progress over time. |
| Athlete | An athlete will design their own workout programs. They need to keep track of their personal progress in addition to making minor tweaks to the program over time. They are basically a trainer with themselves as a client. |

### Problems

The business problem that has the biggest impact to a trainer's bottom line is client count, which is constrained by time. My hypothesis is that decreasing the amount of time spent managing client progress will increase the number of clients a trainer can take on. 

The problem I will focus on for athletes is loss of data. Notebooks are prone to be lost, especially after an intense workout. That along with the generally inconveniences of having to carry pen **and** paper around the gym and trying to log  progress without a decent writing surface.

### Must-have traits of a good solution

1. Tracking progress is **simple AF** - Gyms can be busy environment and workout can often include a time component, so any good solution must support quickly logging progress too avoid derailing the workout.
2. Creating and sharing a workout program is **seamless** - Since I am trying to solve for time, the experience of creating a program and getting it out to clients has to be less painful than the status quo
3. Limited amount of required data entry - Workouts are typically pretty repetive so there is ample oppurtunity to off-load some amount of data entry.

### Market

According to some cursory Google searches, [~58 million Americans have a gym membership](https://www.statista.com/statistics/236123/us-fitness-center--health-club-memberships/), [~8 million high school students play sports](https://www.nfhs.org/articles/high-school-sports-participation-increases-for-28th-straight-year-nears-8-million-mark/), and [~500 thousand college students play sports](http://www.ncaa.org/about/resources/research/probability-competing-beyond-high-school). According to my annecdotal experience, gym-goers range in age from 12 all the way up to 60 (I will eventually get actual stats assuming they are freely available).

The expected number of people who will use the app initially can be counted on two hands. Of the folks who use the app, one will be a trainer, I'd expect him to use it during his training sessions throughout the day, so the app will be used to quickly get to and input information. Each interaction with the app should be less than 15-30 seconds unless the app is being used with a timed workout.
