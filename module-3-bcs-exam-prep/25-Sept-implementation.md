# 25th September 2020
## Morning

### Implementation
#### People Involved
- Users
- Business Analysts - take care of documentation for new software, and can advise engineers on business decisions for releasing software
- Technical Specialists - how software should be released form technical perspective
- Sponsors
- Service Managers

#### Methods of Deploying
##### Big Bang
Everything is deployed at once *crossed fingers it works*

*pros*

- clean start, no depandancies
- less complex and expensive if it works
- do not need to support the phasing out of a previous

*cons*

- high risk of failure
- side effects and bugs are harder to analyse and resolve
- Incredibly difficult to go back and start over



##### Parallel Running
Running new system at the same time as the old one, and slowly phase out the old one

*pros*

- Less risk, can easily fallback to old system
- New system, won't immediately be overloaded with users
- Allows for easy comparison between the versions

*cons*

- Expensive to maintain (double the instances, databases etc.)
- More complex sharing state across systems
- User may not bother using the new system



##### Pilot
Testing out a new system for a handful of users

*pros*

- Gives you the chance to trial the system on a small-scale which minimises risk
- Get feedback to improve software before full release

*cons*

- Won't experience issues on the same scale as the final release
- If software is changed significantly before the release, the pilot might beome irrelevant



##### Feature Releases
Releasing per feature

*pros*

- Easier for people to adjust to the inital software, with minimal features, and will make it easier to adjust to added complexity
- Can release inital software much quicker
- Easy to roll back unwanted or broken features

*cons*

- Users may lose interest in the initial version due to it's simplicity
- Frequently releasing features can be frustrating for users
- User may outright ignore new features

##### Traceability
##### Versioning

*0.0.0* = [ Major Version ] . [ Minor Version ] . [ Patch ]

*semantic versioning*

*major version* Changes that affects the whole system

*minor version* Adds a new piece of functionality of feature

*patches* Minor fixes to software


*alpha* software available internally for testers to try out

*beta* software available to a small handful of end-users

*release* software made available to the public


##### Software Licenses

*proprietary license* closed source software, legally belongs to the individual or organisation that created it - the publisher can grant use of the software to a user through the *end-user license* agreement (EULA), but those actual copies used still belong to the publisher and cannot be modified or distributed by others

*end-user license* A contract between the publisher and a user which outlines the rules for using the software that the user must abide by, and any payment the user has made in order to use the software

*enterprise license* A license given to organisations which enables them to use the software unlimited across the organisation, although they may have to still have some outlined restrictions

*site license* A license that allows distribution of software to mulitple users, as long as they at the agreed site location for the license but may be less costly than having a enterprise license

*workstation license* aka node lock license, which grants the user access to run the software for a specific machine, the software is 'locked' to that workstation

*perpetual license* the 'traditional model' of software distribution, the user pays a one-time fee for access to the software

*open-source license* allows software to be freely used, modifed and distrbuted by anyone



##


__output = Deployed operational software that is available to users__