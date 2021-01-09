# 24th September 2020
## Morning
#### Development

#### Restrospectives
- What worked well?
- What could be improved?
- What will we commit to the next sprint?


#### Version Control
*Benefits*

- Repo to store your code
- Centralised location
- Allow multiple people to independantly work on the same code
- Can view historical data, easier to rollback when there are failures
- Makes it easier to intergrate tools that can be used to improve deployment and intergration


##

__output = written code with functional software, ready for testing__



## Afternoon

#### Testing
##### Why Bother Testing?
- Improve the quality and reliabilty of the software
- Making sure the software meet the requirements
- Providing confidence that the code works
- Adding new features is easier, because when stuff is broken you know that it's due to new changes

*Error* The source of a problem
*Defect* When the logic does not work in the way that it's supposed to
*Failure* A fault in the system where it's unable to run sucessfully


*Pesticide paradox* Same tests will not work forever, because "new bugs will slip through"
*Absence of errors fallacy* Just because it works, doesn't mean that it doesn't have bugs :)


_You should start testing as soon as you have requirements_

*Defect Clustering (Parento Principle) - In a testing context* You will find 80% of your errors in 20% of your code

###### Static vs Dynamic Testing
*Static testing* testing code without running the code
*Dynamic testing* testing code by executing it


*Unit testing* Does the code work in this method/class?

*Integration testing* Does the relevant code work together, does it work as expected?

*System testing* Does the whole system and flow work as it should? (e.g. load teasting, pen testing etc.)

*Acceptance testing* Testing that it meet the business needs/requirements and it can get approval from the end-users

###### Black box vs White box testing
*Black box* Doesn't care how the code executes to get the result, as long as it gets the correct result

*White box* Takes into consideration how the logic operates in the way that it's expected to get the correct result


*Re-testing* Checks whether failing tests that passed in the final execution successfully pass after fixes, tests based on defects

*Regression testing* Test that orginal features work, based on the business requirements and are run to ensure changes have not changed core functionality

*Functional testing* Tests directly against the business requirements


*Non-functional testing* Is it working in a way that is acceptable for it's users

###### Equivalence Partitions/Classes

*Boundary Value Analysis* Testing by using the boundary values of partitions as params for a test


###### Independant Testers vs Internal Testers
*pros*

- free from bias
- different assumptions
- can report honestly

*cons*

- seperate teams can cause hostility
- misunderstanding fo software's goals/usage
- separate team can act as a bottleneck to progress



##

__output = Confirmation that the software meets the business requirements__