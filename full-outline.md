* [SLIDE] The Wall Dev2DevOps

# Beginning
* Hello and thanks for coming to Dev to DevOps. This talk is going to be a high-level introduction to DevOps, from a developers perspective,  and some suggestions of how to get started.
I'm assuming there are probably some people here who are not new to devops,. But maybe, if you can put aside your experience, for a min, imagine that all your code is not being written TDD style; that all your teams are not using CI; that all your deploy are not one button deploys, and all your devs do not have access to VM of the production environment then there may still be some value and entertainment for you here.

* My name is Dinshaw. That's one word; that's my first name. My last name's not really important until you find another person with my first name. What is important is that I work at Constant Contact as a developer and I have nothing to do with operations.
The closest I have come to deployments is complaining when they don't go smoothly.
The code I was working on is deployed on CentOS, and although I worked on this code for over two years, I may have logged into one of our CentOS boxes five or ten times total. Nowhere in my job description does it say I need to know my way around our production environment. And recently, our community is realizing that this is a problem and that the time for change is upon us. Back to that later
...

## Intro
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
* What's does our tool need to look like?
* We need the right tool for a:
1. big job * [SLIDE] - tree and saw
2. Complicated job [SLIDE]
3. Lot of moving parts [SLIDE]
* [SLIDE] Computer
* DevOps refers to these tools
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
** We are supposed to be building the future of the way people organize their lives. 
** But instead, we spend a great deal of time on unplanned work: 
*** configuring the tools and environments
*** And trouble shooting the hand-off to from Dev to Ops
* And the better we get, the more complicated our tool chains and environments become, and fragility creeps into lives.
* Critical systems cannot be fragile
* [SLIDE] Link to talk
*  Why We Need DevOps Now: A Fourteen Year Study Of High Performing IT Organizations
** http://www.youtube.com/watch?v=disjFj4ruHg
* I'm taking a lot of things from this presentation
* High Performance Organizations
** Using Version control and automation to ship [...] applications quickly without disrupting service
** deploy code 30 times more frequently than their peers
** completing those deployments 8,000 times faster
** 50 percent fewer failures.
** restoring service 12 times faster.
* Puppet report http://info.puppetlabs.com/2013-state-of-devops-report.html

## The Solution
* The dream is that, all day, all we have to do is 'our jobs'
* That our work moves from left to right, through our entire system, business–requirement to production, with very little exception
* DevOps refers to the tools and the mindset that aspire to keep our systems efficient, and to enable us to keep applications available while constantly introducing significant amounts of change. 
* Responsibility falls on Developers in that we now need to own both the development of our software, and also the operation of it.
* Responsibility falls on Operations to provide us with the tools that we need to do this.
** One button environment
** One button deploy
* Responsibility falls on everyone to start the dialog. To  begin to collaborate and to cooperate.
[SLIDE] - Holding hands
* And this collaboration and cooperation is the 'Culture' of DevOps that is going to save us all, and that's great, but !!!
* [SLIDE] Culture
* What's that you say? But culture is not going to get me past the butthole...
* [SLIDE] Buthole
* [SLIDE] Fuck Culture
* Give me tools
[SLIDE] - Tools
* Tools I can use
* [SLIDE] G'Tool, whoops... Computer 
* Common tools
* Because common tools will not only be more efficient, but also help to heal the rift. To tear down the wall
[SLIDE] TEAR DOWN THE WALL
* I'm gonna talk about some good tools to check out shortly, but a quick example of common tooling is that developers and operations, and really the whole organization, should be using the same version control system. If something happens in the middle of the night, and everyone knows where to look, has access, and knows how to use the tools to say: do a version bump, then one less person gets woken up, one less person is grumpy the next morning, and everyone wins.
* Not just refactoring legacy code anymore, we are refactoring legacy organizations and the way we work.
* And as we refactor code, we succeed when it is easy to change the code without breaking anything. This is important because our job, as a developer, if you had to sum it up, is introducing change.
* We need systems that are capable and comfortable existing in a constant state of change.
* This is so far from where a lot of organizations are today, that in the Why We Need DevOps Now talk, Gene Kim says:
You need a culture that keeps pushing into the danger zone  
And has the habits that enable you to survive in the danger zone

## Contrast
* So from a developer's point of view, what does this look like?
* A couples examples
* We all have our development machines setup differently. The software we use and our configurations are the tools of our trade. And just like a chef and his knives, this is a very personal thing. We put a lot of time into getting everything just right. THis is important because it directly effects our state of mind, and our emotional state (!!!) when we sit down to work. This is great, but i'm sure we've all been ready to push some code on friday afternoon, we merge in master, bundle install, and everything blows up. An hour later, if you're lucky, you realize it is because someone added a gem that doesn't build with the light-weight GCC that we  installed 'to save time'. This is a trite example but the problem is clear: the discrepancies between one or more developers environments have needlessly cost us time and energy.
* Does anyone here have a script that they use to set up their dev machine?
* A lot of us have probably toyed with the idea of a setup script to provision our personal computers. maybe a shell script, or Chef, or Boxen, both of which I will talk about later, and even if we haven't done it, this seems totally reasonable because we will probably want the same tooling on all my machines.
* Now what if someone suggested that you share a setup script with your team? Or possibly your entire organization?
* Sounds crazy, right?
* Unless…
* Unless this script was well written, overridable, extendable, and in available in version control.
* Then, we can login, read the base setup script, fork it, add our customizations on top of it, and fire it off knowing that your gcc will be the same as everyone else's and that version bumps and other common stuff will be pushed out via your organization's base class.
* This is where we are trying to get to. All the benefits of the collective wisdom, with zero sacrifice of individuality

### Project Environment
* OK, so in the perfect world i just described i pull down my code knowing that
my system-level tools are the same as everyone on my teams, install my gems, run my spec, and everything is still broken...
* Turns out someone added Redis to this project. This is not a system level tool,
this is a per-project dependency.
* its also not too hard to debug, but that is not always the case.
* Git pull; bundle is not enough for any real–world project
* But just like Server definitions, there can be project definittions that install the proper runtimes and data stores and fetch the latest code and do a better job of ensuring consistency across multi–developer teams
* [SLIDE] : Boxen project recipe

### CI and CD
* Everyone in this room is familiar with problems running code on CI and in Production, so i will skip enumeration of my many battles.
* The take away here is that these issues that we all see and accept as 'part of our job' are avoidable.
* If your development or your local test env is a VM that is exactly what is running on CI and Prod, then the time we spend troubleshooting these issues largely goes away.

!!!
* We start to automate our lives
* [SLIDE] - Gerbils holding hands
* To take advantage of these tools, now, is to leap into the future of our industry.
* Worlds which were separated by a wall, will be peacefully dismantled by common toolsets, and common goal, of DevOps
* Shadow IT - everyone managing their own shit because it takes to long the 'right' way

## And we become viable as Talent
* Puppet and OpsCode
* Puppet report http://info.puppetlabs.com/2013-state-of-devops-report.html
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
* Well, our lack of time and other priorities is an easy answer, but also, its overwhelming. Its a little scary to have to be a beginner again. We learn all day, learning a new gem is easy. A new way of doing things takes a little more effort.
* 10 Years of martial arts story
* So we decide to start but we are supposed to be professionals and now we are muddling though like beginners again.
* [SLIDE] Muddle
* Muddle quote...
* Alternative is to carry on down the wrong road. and we all know...
* I'll tell you what should be even scarier: getting left behind

## How do I start?
* So as a developer, how do I move to CD?
* Dev & Test are no longer separable.
* Not doing TDD? You will NEVER get to CD.
* Zero (0) manual QE _in the deployment workflow_. Everything has to be automated.
* WOrking code AND the env it runs in
* Ops must provide a one button environment
* One button deploy; one button environments.
* Developers do the deployment
* Developers own uptime for code; Operations own uptime for platforms and tooling
* You build it; you run it.
* Google SRE - Hand-off Readiness Review
* break things before prod
* Run tests in 1000 servers - must be an automated set up. not hard if your env setup is a 1-click operation
* Choas Monkey - ec2 outage - break things before production
* 20% of all cycles should be allocated to technical debt
* Show the Scott Cook's:
By installing a rampant innovation culture, they now do 165 experiments in the three months of the season.

Our business result? Conversion rate of the website is up 50 percent. Employee result? Everyone loves it, because now their ideas can make it to market.
* After introducing the problem they put up a slide called 'Tools' and the number one thing they site is 'Automated Infrastructure'
* No Such THing as DevOps Team - http://continuousdelivery.com/2012/10/theres-no-such-thing-as-a-devops-team/
Create reusable deployment procedures: When every deployment is done differently, every production environment can become different, like snowflakes. When this occurs, no mastery is ever built in the organization in procedures or configurations. As Luke Kanies said, “If your infrastructure is special, you’re doing it wrong.”
!!! What gets measured gets managed: the transparency that comes with automation will show that there is nothing special going on...
* automate one small, familiar thing that already works
** Remove whitespace from files in your editor
** Set up .dotfiles
** Empty the trash on your computer
** Dev machine set up
** Dev virtual machine set up
* as we automate, we will go deeper, develop a more intimate relationship. cooperate with our machines. We automate the things we know, then we don't have to think about that again and we can move further.

### Larger scale: project or company
* Start with the most critical end-to-end flow
## Tools/Techniques/Ideaologies
* Puppet - http://puppetlabs.com/misc/webinars/?aliId=8052887#learningpuppet - On demand webinars
** Boxen
* Chef
* Pair-Programming
* http://dev2ops.org/
!!! more
* Have coffee with an operations person
* Take DONE off the Kanban board: Code-Completion is an anti-pattern. We build and run services; the best we can hope for is that we have fulfilled our most recent obligation
* Amazon @ O'rily Velocity Conferance - June 16, 2011
http://assets.en.oreilly.com/1/event/60/Velocity%20Culture%20Presentation.pdf
11.6 seconds - Mean time between deployments (weekday) 1,079 - Max # of deployments in a single hour 10,000 - Mean # of hosts simultaneously receiving a deployment 30,000 - Max # of hosts simultaneously receiving a deployment

## Where do i end up?
* It is a lot to learn but the payoff is currently unlimited
## Reward
* Personal
!!!
* Business
!!!
* Global/World
!!!
* Want to do something well, do it more often
* The longer you do devops, the better it gets

## Pay-off
* Twitter Murder
* Google SRE - Hand-off Readiness Review
** Types/frequency alerts
** Maturity of monitoring
** System architecture review
** Release process
** Defect counts and severity
** Production Hygiene
* Chat Ops

## Conclusion
* Restate !!!
* DevSecOps?
* Slides

## Links
http://continuousdelivery.com/
* Puppet report http://info.puppetlabs.com/2013-state-of-devops-report.html
* Chatops slides/talk


“If you tell the truth, you don't have to remember anything.” 