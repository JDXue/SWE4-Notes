# 29 Oct
## Morning

*Side Note : Probably should go over CSS and HTML again!*

#### CSS Styling in JSX

*Example*
``` js

<button style = {{
    backgroundColor: 'green'
    }}>

```

JSX styling requires double curly brackets because it is parsed in nested in two js objects


CSS Properties are also different because they are in JS - the same CSS properties can be used, but the React

*look updn AirBnB React guide for their in-house use*

**Spread operator can often be used to create a copy of a multidimentional array where you want to manipulate an element, however the copy of the array will still have it's original array copied from the first in the sam eplace in memory, so be careful when manipulating the copied elements**

**To avoid this, you can spred the array while nested in another array:**

``` js
const arr = [[1,2,3],
            (4,5,6)]
const newArr = [[...arr[0]],[...arr[1]]]

```

#### Creating Multiple Similar Components with .map() - Example


``` js
boardContent.map((cellContent, index) =>
return (
    <Cell
        //when creating multiple components at once, you  must include a value called 'key' that gives each an id when used in the virtual DOM to help React keep track of what has changed
        key = {index}
        content = {cellContent}
        index= {index}
        updateForGivenIndex = {}
    />
    )
)



```

**Lifting States**  When states created within a component are needed higher up in the heirachy of components within the application


