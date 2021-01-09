# 21st September 2020

## Morning

### Software Development Lifecycle (SDLC)

#### 1. Feasibility Study
*purpose of study*

Understand whether a project is should be initiated, understand the business, legal, financial, technical considerations of the project

*who is involved*

Generally senior and business areas of the business

#### 2. Requirements Analysis
- what needs to get done to complete the project?
- identifying additional features form MVPs?

#### 3. Design

*purpose of the stage*

Designing how the software will work (e.g. technical, structure, layout) - UI and UX

*output of stage*

Wireframes, UML diagrams plus other documentation outlining how the software will be built
*who is involved*
Developers, Business experts, stakeholders
*technique, tools involved*


#### 4. Development
*purpose of the stage*

- Creating the solution based on identified problems or need for new features
- Understand the data structure
- This is the section that we should (typically) be most familiar with


#### 5. Testing
- Test against requirements
- Does it work how we expect it to?

*purpose of the stage*

This stage is the process of making sure the software works, and that it has met the initial objectives outlined in the Requirements Analysis stage, as well as to the requirements of the end-user. This can be done in a number of ways, but this is normally carried out by writing unit tests, possibly also combined with integration tests (testing a user path in an automated test). Tests are written to provide confidence that the code will work as expected when deployed, therefore they are created to satisfy the targets set in the requirements stage.


*where it fits in the cycle*

This comes after the Development stage, where the software is created

*output of stage*

The result of this stage is basically proof that the software works and can be used in the implementation stage to ensure that deployed versions of the software going out to the production environment is able to meet an acceptable level of reliability

*who is involved*

In theory, it is the QA team of an engineering group who carries out this stage, however, it's more common for developers to write their own tests and test that their code works before the Implementation stage

*techniques, tools involved*

Most common are automated testing suites (e.g. Jest, Chai, Junit) that are libraries where developers can explain the expected outcome of the code. Testing can also be carried out by getting real end-users to test the software in alpha and beta versions of the software not yet released publicly (user acceptance testing) - this requires the deployment of newer versions made available to people within the organisation, or to exclusive external users of the product


#### 6. Implementation
*purpose of the stage*

- Make software available to end-user
- Release, deploy and run
- User has access the software

*who is involved*

Developers, operations, senior devlopers, business approvers/advisors

*techniques, tools used*

- Pipeline managers, instance rolling managers etc.

#### 7. Maintenence
`...`


## Afternoon

### Waterfall vs Agile

#### Waterfall
Every stage is highly documented, you can't move forward to the next stage until the previous stage is complete


*Pros*
- Straight forward and logical
- The final end-product should be of high-quality since each stage is rigorously assessed and highly documented


*Cons*
- If a later stage of the cycle does not meet the requirements of the design or the clients, you will have to start again from an earlier stage which is very time consuming
- Focusing on each stage makes it take a long time to complete, and can be very costly
- Takes a long time to get to the user
- Doesn't respond to change well


*Usage*
- When requirements are clear and do not have much room for rectification
- Projects you can ensure you'll be able to get right first time without prototypes


#### Agile
Result of engineers in the 90s who created an "Agile Manifesto" - some principals outlaying a new way of defining the software development cycle which is less susceptible to change. Agile will have sprints, which are stages where a small part of the product is built, that are completed every 2-4 weeks roughly

*Pros*
- More stakeholder involvement in the process and customer collaboration
- Responding to change is very easy
- Allows developers to reflect on the previous sprint which can help to understand the process
- Much easier for developers to test iteratively
- Deployments of code have fewer risk dues to small amounts being deployed each time
- Software can be recieved by users quicker, and feedback can be recieved quicker, which can reduce the time to make changes in response to the client

*Cons*
- It's harder to define where the end of the project is
- You will find it harder to know what the end-product looks like
- Documentation will constantly need to be updated or might just get ignored

*Usage*
- Projects where the requirements have the change often, clients have a tendency to revise their needs
- Projects that can easily define an MVP
- Small-scope projects


#### Extra: V-Model

- Linear development alike waterfall
- Each stage of design is associated with a type of testing
- Essentially TDD

*Pros*
- Additional testing can get a high-quality product
- Easy to scale
- Easy to project manage
- Rigid dev cycle --> neglecting designing or testing can make the methodology fall apart

*Cons*
- Heavy testing is expensive
- Devs can get lazy and ignore some of the stages
- Earlier stages take longer


*Usage*
- For projects that are critical to work the first time


#### Exra: Incremental
`...`

### Agile: DevOps
https://docs.google.com/presentation/d/1u1FT9NGP1faa2FOPd3oFoGuKOFvKkeVmA2jUD8PM__o/edit?usp=sharing

### Agile: Kanban
- Better for less time-crucial tasks
- Identifies the long-time productivity

### Agile: Scrum
- Identifies the short-term, focused deadlines
