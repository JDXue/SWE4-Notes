# 29 Oct

## Morning

### Introduction to React
npm = Node Path Manager (locally)
npx = (cloud based)

#### JSX
JSX is eventually compiled as HTML, but it allows you to add JS scripts within it to change the html depending on certain conditions

function components are often easier to read and generally perfom better

**you should not mutate elements in JSX, because React does not work well with mutations**

Because of this, you use useState(), which allows you to make changes to a const via a function that is the second parameter passed in

``` js
   //example
     const [hand, setHand] = React.useState([10,5]) //hand is the array variable, and setHand is used to change the state of hand without mutating the original variable

    //then you can change the const with the state later on
    <button
        //button should add 3 to hand when clicked
        onClick = {() =>


        setHand(hand.concat([3]))}>
```

**React custom elemetns use capital letters to differntiate from HTML elements**


**there are two ways of assigning a const as props (props is an object from which you can reference inside functions)**

**Component** A single function/ class that will execute a set of actions when called

*It's common to put components in separate files and call each to one App.js file via import ComponentName from './path-in-app-dir'*

**Make sure to use import React and export the componets for use!**


Props is a good way fo passing down elements and properties from parent to child

Passing elements in the reverse is rare but would often need callbacks
``` js
const total = props.total
const { total } = props

```
React fragments are an alternative to div elements. which is slighly better to use when div is used as a container to avoid errors when rendering, because it doesn't show up in the element tags

*Fragments can be used with an empty tag in React <></>*



```js


```