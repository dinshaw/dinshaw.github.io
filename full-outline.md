* [SLIDE] The Wall Dev2DevOps

# Hello and thanks for coming to Dev to DevOps.
This talk is going to be a high-level introduction to DevOps, from a developers perspective,  and some suggestions of how to get started.
I'm assuming there are probably some people here who are not new to devops,. But maybe, if you can put aside your experience, for a min, imagine that all your code is not being written TDD style; that all your teams are not using CI; that all your deploy are not one button deploys, and all your devs do not have access to VM of the production environment then there may still be some value and entertainment for you here.

* My name is Dinshaw. That's one word; that's my first name. My last name's not really important until you find another person with my first name. What is important is that I work at Constant Contact as a developer and I have nothing to do with operations.
The closest I have come to deployments is complaining when they don't go smoothly.
I have never logged into a CentOS box, which the application that I worked on for the last two years runs on. This is a problem. It's also not entirely true, I have logged into one of our CentOS boxes a long enough to tail a log, figure out there is nowhere to run 'rails c'	 in a jruby deploy, and then run out of space for my minimally provisioned user.
My job description does not say that I need to know my way around our production environment. And recently, our community is realizing that this is a problem and that the time for change is upon us. Back to that later...

## Law of the Instrument
* [SLIDE] Law of the Instrument
* Law of the Instrument Abraham Kaplan, American Philosopher 1918-1993 in 1964
* [SLIDE] Hammer
If all you have is a hammer, everything looks like a nail
* [SLIDE] Nail
* Nails aren't that bad. I know how to use them; they work; I can deal with this problem.
* [SLIDE] G'Tool (Guitar-tool)
Does anyone recognize this?
It does everything you could ever want to do to your guitar.
So then if all I have is a G'Tool, do all my problems look like a guitar? Guitars are fun! I like this problem...
* [SLIDE] Flaming guitar
* [SLIDE] Monster / butthole
* So now if our problem looks like an army of multi-armed-vampire-butthole-beasts?
* Our problem is scary!
* [SLIDE] Computer
* We are going to need more than one tool…
* [Slide - Hammers]
* We need the right tool for a:
1. big job * [SLIDE] 
2. Complicated job [SLIDE]
3. Lot of moving parts [SLIDE]
* [SLIDE] Computer
* DevOps refers to not so much a tool, as mindset that finds the best tool for the job so that we can !!!
* [SLIDE]- Cause of and solution to all of life's problems

## History
* At the dawn of the computer age, there was no distinction between dev and ops. You mounted tapes, you flipped switches, and you wore a lab-coat.
* [SLIDE] - Colosus
* And then came the punch cards; that you handed over to an  'operator' who delivered a printout to a cubbyhole with your name on it.
* [SLIDE] - Punch Card
* And then finally, the arrival of the PC completely separated  operation from user and the modern 'IT Operations' culture was born, and the wall began to go up...
* [SLIDE] The wall goes up
* 2007 Patric Dubois, Ghent, Belgium wanted to work in every possible area of IT
* [SLIDE] Velocity conf link
* 2009 Velocity Conf San Jose (http://velocityconf.com/velocity2009)
Web companies of all sizes face many of the same challenges: sites must be faster, infrastructure must scale, and everything must be available to customers at all times, no matter what.
** 10+ Deploys Per Day: Dev and Ops Cooperation at Flickr
*** John Allspaw and Paul Hammond
* [SLIDE] Talk link
* The community knew there were problems, but these guys really called it out and gave it a face, if not a name, and showed a path to salvation.
* That there was, and still is, a common rift between developers and operations. THere was a lack of trust and a  lack of respect. And it was self-perpetuating, and only getting worse.
* Developers job is to add new features; Operations job is to keep the site stable and fast
* [SLIDE] Devs who think like Ops / Ops who think like Devs
* This was the beginning of the DevOps movement, even though the name hadn't been given.
* Dubois missed it!
* Chatting on Twitter, people said you should start your own Velocity conf
* Dubois organizes DevOpsDays 2009 in Belgium - Ghent
* [SLIDE] DevOpsDays link
** Talks like
*** 'Introducing Kanban in operations'
*** Continuous Integration, Pipelines and Deployment
*** Building Agile Infrastructures with Puppet
* Twitter dropped the 'Days'
* Grassroots movement against legacy tools and culture
* From practitioners, for practitioners
* NOT a 'thing/spec/product/standard/job-title'
* a lot of people collaberating on common problems
* #devops on twitter still has lots of valuable

## The Problem
* As a professionals in the software industry, our job is to:
** Deliver value to our end users by innovation
** We are supposed to be conceptualizing and building the future of the way people organize their lives.
* But the reality is that we spend a great deal of time on:
** Unplanned work
** Configuring and fixing our tools and environments
** And trouble shooting the hand-off to from Dev to Ops
* And the better we get, the more complicated our tool chains and environments become, and fragility creeps into projects and lives.
* Critical systems cannot be fragile
* [SLIDE] Link to talk
* Why We Need DevOps Now: A Fourteen Year Study Of High Performing IT Organizations
* I'm taking a lot of things from this presentation
* High Performance Organizations
** Using Version control and automation to ship [...] applications quickly without disrupting servicez
** deploy code 30 times more frequently than their peers
** completing those deployments 8,000 times faster (1 min deploy vs 1 week deploy)
** 50 percent fewer failures.
** restoring service 12 times faster
* Those are some pretty compelling numbers

# The dream is that, all day, all we have to do is 'our jobs'
* That our work moves from left to right, through our entire system, business–requirement to production, with very little exception.
* DevOps refers to the tools and the mindset that aspires to keep our systems efficient, and to enable us to keep applications available while constantly introducing significant amounts of change.
* New responsibility now falls on Developers in that we need to own both the development of our software, and also the operation of it.
* Responsibility falls on Operations to provide us with the tools that we need to do this.
* Responsibility falls on everyone to start a dialog. To  begin to collaborate and to cooperate.
[SLIDE] - Holding hands
* And this collaboration and cooperation is the 'Culture' of DevOps that, as you may have heard, is going to save us all.
* [SLIDE] Culture
* What's that you say? But culture is not going to help you with your current problem.
* [SLIDE] Buthole
* You are totally right
* [SLIDE] Fuck Culture
* Give me tools
[SLIDE] - Tools
* Tools I can use
* [SLIDE] G'Tool, whoops... Computer
* And more specifically,, give me _Common_ tools
* 'Common', because if we are all using the same tools we will get better at them quicker, but also because a common toolset fosters the colaberation and cooperation that will lead to the trust and respect. To tear down the wall
[SLIDE] TEAR DOWN THE WALL
* I'm gonna talk about some specific tools to check out in a minute, but one example of common tooling is that developers and operations, and really the whole organization, should be using the same version control system. If something happens in the middle of the night, and everyone knows where to look, has access, and knows how to use the tools to say: do a version bump, then one less person gets woken up, one less person is grumpy the next morning, and everyone wins.
* Not just refactoring legacy code anymore, we are refactoring legacy organizations and the way we work.
* When we refactor code, we succeed when it is easy to change the code without breaking anything. This is important because our job, as a developer, if you had to sum it up, is introducing change.
* We need systems that are capable and comfortable existing in a constant state of change.
* This is so far from where a lot of organizations are today, that in the Why We Need DevOps Now talk, Gene Kim says:
You need a culture that keeps pushing into the danger zone
And has the habits that enable you to survive in the danger zone.
* Intuit's Scott Cook at the Economist conference 2011 Talking about when TurboTax:
By installing a rampant innovation culture, they now do 165 experiments in the three months of the season. Our business result? Conversion rate of the website is up 50 percent. Employee result? Everyone loves it, because now their ideas can make it to market.


## So from a developer's point of view, what does this look like?
* A couples examples
* We all have our development machines setup differently. The software we use and our configurations are the tools of our trade. And just like a chef and his knives, this is a very personal thing. We put a lot of time into getting everything just right. THis is important because it directly effects our state of mind, and our emotional state (!!!) when we sit down to work. This is great, but i'm sure we've all been ready to push some code on friday afternoon, we merge in master, bundle install, and everything blows up. An hour later, if you're lucky, you realize it is because someone added a gem that doesn't build with the light-weight GCC that we  installed 'to save time'. This is a trite example but the problem is clear: the discrepancies between one or more developers environments have needlessly cost us time and energy.
* Does anyone here have a script that they use to set up their dev machine?
* A lot of us have probably toyed with the idea of a setup script to provision our personal computers. maybe a shell script, or Chef, or Boxen, both of which I will talk about later, and even if we haven't done it, this seems totally reasonable because we will probably want the same tooling on all my machines.
* Now what if someone suggested that you share a setup script with your team? Or possibly your entire organization?
* Sounds crazy, right?
* Unless…
* Unless this script was well written, overridable, extendable, and in available in version control.
* Then, we can login, read the base setup script, fork it, add our customizations on top of it, and fire it off knowing that your gcc will be the same as everyone else's and that version bumps and other common stuff will be pushed out via your organization's base class, but all your personal stuff will be just the way you like it.
* This is where we are trying to get to. All the benefits of the collective wisdom, with zero sacrifice of individuality

### Project Environment
* OK, so in the perfect world i just described i pull down my code knowing that
my system-level tools are the same as everyone on my teams, install my dependancies, run my tests, and everything is still broken...
* Turns out someone added Redis to this project. This is not a system level tool,
this is a per-project dependency.
* its also not too hard to debug, but that is not always the case.
* Git pull; bundle install; is not enough for any real–world project
* But just like Server definitions, there can be project definittions that install the proper runtimes and data stores and fetch the latest code and do a better job of ensuring consistency across multi–developer teams
* [SLIDE] : Boxen project recipe

### CI and Production
* I am guessing everyone in this room has experienced problems promoting code from a development environment to CI and Production, so i will skip the example here.
* The take away here is that these issues that we all see and accept as 'part of our job' are avoidable to some extent.
* If your development environment and your local test environment are identical to CI and Production, then the time we spend troubleshooting these issues is minimized, and, maybe more importantly, the frustration and the finger–pointing 'hey it worked on my machine, it must be your fault' is also minimized.

## And we become viable as Talent
* In addition to being happier and more productive, DevOps skills will keep us viable.
* We are all incredably fortunate to find ourselves in a seemingly recesion proof industry.
* [SLIDE] Working is the new rich
* DevOps is where our industry is heading. Our job description is changing and it is up to us whether we answer the call or not.
* Puppet report http://info.puppetlabs.com/2013-state-of-devops-report.html
* [SLIDE] State of DevOps Report
* LinkedIn keyword 'DevOps' up 50% from 2012 to 2013
* DevOps is: - from Puppet Blog - https://puppetlabs.com/blog/what-is-a-devops-engineer/?utm_campaign=newsletter&utm_medium=email&utm_source=newsletter-201306&utm_content=0523earnshawdevopsengineer&mkt_tok=3RkMMJWWfF9wsRokvK%2FKZKXonjHpfsX64%2BkpUaO2lMI%2F0ER3fOvrPUfGjI4CTsdiI%2FqLAzICFpZo2FFID%2FCFeZRM%2B%2FdO
** Coding Scripting
** Process Reengineering (seeing how/where it could be better)
** Communication and collaboration
** Comfort with with frequent, incremental code testing and deployment
** Strong grasp of automation tools
** A strong focus on business outcomes
** Comfort with collaboration, open communication and reaching across functional borders

## Our Reluctance
* Why aren't we doing all this already? Been around since 2007.
* Why isn't everyone doing TDD and CI? It's been around for a while now. Everyone agrees its the right thing to do.
* Well, the easy answer is:
** No time! Too many other priorities...
* We are paid to be professionals, and in some cases, experts. To know what we are doing. And for the
most part, we do. We also have a great deal of learning baked into our day-to-day.
* We learn new libraries to use in our code-bases all the time.
* But a new set of tools and a new way of working is going to take a little more effort.
* It can be pretty overwhelming think about being a beginner again.
* [SLIDE] Overwhelmed
* Muddle story…
* This is the right way to feel. It means that you are pushing the edges of your comfort zone and that you are learning. Dont be afraid to hit enter...


## So what is the first step, and how do I make it fun?
* One of the two similarities of the High performing organizations that Gene Kim speaks about is Automation; the other one being version control.
* Automation is a great place for any developer to start
* Take one small, familiar thing that you already know how to do, and automate it
** Make sure your editor removes white space when you save
THis might be a simple as setting in your preferences, but that is automation and if it works consistently, then it is valuable forward progress.
** Set up .dotfiles
** Setup a task to rotate your development logs before your machine runs out of space
* These things might seem trivial, but when we start to automate away the little things that take our time, we start to expose the next level of opportunity for optimization of our workflow.
* You will start to see opportunities to automate everything
** Automate the setup of your development environment, the way you like it. Don't worry about sharing it with anyone else.
** Automate the setup of your production environment; and then do it as your development workstation.
* [Slide] Puppet & Chef 
* [SLIDE] Puppet
** Run by Puppet Labs
** Written in ruby
** Define the state that you would like you machine to be in.
** Idempotent - Run it over and over and you will always end up in the same state
** [SLIDE] Boxen
*** link to presentation on the last slide
*** Github wanted to make sure that everyone could push code their first day
*** Run it often
*** Security patches pushed out via a pull request
*** Works out of the box, but still some kinks
* [SLIDE] Opscode Chef - link to presentation
** Chef server
** Chef solo
** Chef tools
* So when we have used automation to help ensure that our machines works the way we want them to, we can start thinking about stuff a little further up stream like, 'does our code work the way we want it to?'
* The time has come to be ashamed, if we are not doing TDD
* I cannot even imagin working with untested code anymore. I would lose my hari and then my mind.
* [SLIDE] If you tell the truth, you don't have to remember anything.
* Every line of untested code that we write, is like a lie that we tell to our boss that we forever have to remember. This is no way to live and its no way to work
* Dev & Test are no longer separable.
* Not doing TDD? You will NEVER get to CD.
* Manual testing has no place in the deployment workflow. Zero (0) manual QE _in the deployment workflow_. Everything has to be automated.
* Once we know our code is solid, we can begin to address the environment.
* Working code AND the env it runs in
* Two things we need from ops:
** Ops must provide a one button environment that you can be 100% confidant is a clone of your test production environment. This becomes possible when setup of these environments is scripted with something like Chef or Puppet, and under version control
** One button deploy: we have to know that deployments are happening the same way every time.
When every deployment is done differently, every production environment is different and no mastery procedure or configuration will ever be achived.

* Developers do the deployment
* Developers own uptime for code
* [SLIDE] You build it; you run it.
* Google SRE - Hand-off Readiness Review
** Types/frequency alerts
** Maturity of monitoring
** System architecture review
** Release process
** Defect counts and severity
** Production Hygiene
* When we get here, we can start forseeing common production issues before they ever get to production. Break things before prod
** Choas Monkey - ec2 outage - break things before production

* Pair-Programming
* Maybe even from someone from the other side of the wall
* Have coffee with an operations person

## Pay-off
* Twitter Murder
** had a Git-based deploy system where we’d just instruct our front-ends to download the latest code from our main git machine and serve that. Oonce we got past a few hundred servers, things got very slow
** Customized Bittorent running inside their datacenter
* Chat Ops
* Amazon @ O'rily Velocity Conferance - June 16, 2011
http://assets.en.oreilly.com/1/event/60/Velocity%20Culture%20Presentation.pdf
11.6 seconds - Mean time between deployments (weekday) 1,079 - Max # of deployments in a single hour 10,000 - Mean # of hosts simultaneously receiving a deployment 30,000 - Max # of hosts simultaneously receiving a deployment

