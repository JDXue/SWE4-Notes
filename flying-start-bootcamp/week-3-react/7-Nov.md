# 7 Nov
## Morning

### Using Router in React

Router is used for displaying diffent pages of an application. The most popular router is React Router.

**Installation**

```
npm install react-router-dom --s
```

<Router> must go on the outside of components to be routed

<Route path=''> enables you to specify a new page forn the routed components

<Link to='{path}'>{description}</Link>


**Alternative - Using History**

```js
const history = useHistory()
history.push('./path_name')
```

**Make sure links are outside switch component if they need to be on every page**


```js
<Route exact path='/.....'>
```

or

```js
<Route exact=true path='/....'>
```

will resolve problems with path name that both contain the same initial path

