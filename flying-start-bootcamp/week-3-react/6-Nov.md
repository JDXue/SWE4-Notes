# 6 Nov
## Morning

### useEffect Continued
#### Why use dependancy arrays?

Dependancy arrays allow for the user to provide conditions in which useEffect (as in use side effect) will be executed.

Having a no dependancy array in useEffect means that useEffect will re-run every time any state updates.

***If there are any states updating within useEffect, it will cause it to go into an infinate loop, because the state in the useEffect being executed will always be different to the state in the past render***

Having an empty dependancy array does the opposite to having no depandancy array, since it sets the condition that useEffect will not re-render when any state is changed.

By default, it shoudl run only once, when the component is mounted

## Afternoon

### APIs with useEffect

### Installing Axios

```
    npm install axios --save
```

Using ***--save*** installs the package and adds it as a depedancy to the application in the package.json file, which mean that if another person downloads the program onto their computer and runs npm install, the package wll be downloaded automatically.

#### Promises and Async Functions

* Promises come from async functions that have not yet executed all of it's code

* ***.then()*** is used for when the promise of an async function is carried out  (fulfilled)

* An alternative solution is to define a function as asynchonous with ***async*** and use ***await*** to execute code that need to be run after the asynchronous code


#### Classes vs. Functions

```
componentDidMount() + componentDidUpdate() = useEffect(() => {setState(state)}, [state])

```

useEffect runs when:
1. Component mounts (initialised)
2. State is updated



**Recommended**
If a state is changed in useEffect() or a useEffect has a state as a dependency, put useState and useEffect functions next to / near one another






