# 11 Nov
## Morning

### Intro to Redux

Redux was created to try and prevent states from being mutated accidently, and makes it easier to access state values from deep children components.

**A condition that uses the or (||) operator where the first value can be falsy, the second value will be put in action**
Example:
```js
const myVar = undefined || 'value'
```

#### Store
Store will store a state tree, which is an object that holds several state values for the application


**Used in the Parent File**
```js
createStore(reducerName)

<Provider><ParentComponent></Provider>
```

**Used in Children Components**
```js
useSelector(storeState)

useDispatch()
```

#### Reminders Example

* [x] **Version 1 - MVP**
    * [x] Display reminders
    * [x] User is able to add reminders to a list via input box
    * [x] User can delete reminders

* [ ] **Version 2 - Add Reminding Feature**
    * [ ] Allow user to assign a day to remind
    * [ ] Allow user to assign date and time to a reminder
    * [ ] Only show reminders that have an assigned reminder time
    * [ ] Allow users to delete all reminders

* [ ] **Version 3 - Add Backend**
    * [ ] Save state tree to firebase
    * [ ] Associate reminders to a user account

