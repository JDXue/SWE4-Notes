# 5 Nov
## Morning

### Refactoring and React conventions

* Give components names that desribe what they are displaying
* A new component should only be made if they are displaying something to the screen
* If component props are getting too long, they should be placed above the component in an object
* If a component is getting very big, it is recommended to split it into sub components
* Ternary functions should only have a one line statement


## Afternoon

**useState uses a callback array when the value is incremented/decremented**

### useEffect

Without a dependacy array, useEffect renders every time there is an update to a state in the component

#### Clean Up Functions

___For working with APIs and asynchonous functions__

* Create a function inside useEffect function

* By returning a clean up function, it checks for code that is only half completed (not yet executed) and cancels it out and leaves the most current update to the application in the queue to exexute









