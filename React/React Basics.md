
React is a JavaScript library based on COMPONENTS, chunks of user interface.

### Why & when should I use React?
The hole propose is to make the process of front-end easier. Learning React make your code cleaner in a short period of time instead of only using pure JavaScript. It's design to make your life easier.
The reason to use React is the the same to use Flask, Bootstrap, SASS, etc. It is about making your life easier, so you don't need to build everything from scratch.

### Now you learn the React Basics, you should go to [[React Advanced]].
---

### Get started in seconds
1. Create react app using the terminal
```
npx create-react-app my-app

npm install
npm start
```
2. Create a react app using Vite (Recommended)
```
npm create vite@latest my-app -- --template

npm install 
npm run dev
```
---

### Folder structure
- #### Node modules:
	### Folder that contains all dependencies required by the app.
- #### Public:
	Contains static assets including index.html and the entire application (id="root").
- #### Source:
	Brain of our app, index.js.
- #### package.json:
	Useful info about the project.
* #### package-lock.json:
	A snapshot of the entire dependency tree.
* #### README.md:
	Info file to share more info about project.

### JSX Rules:
- return single element (one parent element)
- camelCase property naming convention
- className instead of class
- close every element
- formatting

### How to import CSS:
- create index.css in src
- import file and add classes
```js
import './index.css';
```

### Local Images:
- external images (hosted on different server) - just need an url
- local images (public folder) - less performant
- local images (src folder) - better solution for assets, since under the hood they get optimized.

### Props:
```js
//rops basic example:
const title = "banana voadora mortal"
const Component = (props) => {
	return <h1>{props.title}</h1>
}

<Component title={title} />

```
The props are passed as a OBJECT, so...
```js
//Props with several values example:
const name = "jao"
const age = "19"
const hairstyle = "moicano"

const Person = (props) => {
	const {name, age, hairstyle} = props
	return (
	<> %%You can not return multiple elements%%
		<h1>{name}</h1>
		<h2>{age}</h2>
		<h2>{hairstyle}</h2>
	</>
	)
}

OR

const Person = ({name, age, hairstyle}) => {
	return (
	<> //You can not return multiple elements
		<h1>{name}</h1>
		<h2>{age}</h2>
		<h2>{hairstyle}</h2>
	</>
	)
}

<Person name={name} age={age} hairstyle={hairstyle} />
```

### Children Prop:
It is a special prop, don't write "Children", must write "children". It is used for inside content.
```js
const Person = ({name, age, hairstyle, children}) => {
	return (
	<> //You can not return multiple elements%%
		<h1>{name}</h1>
		<h2>{age}</h2>
		<h2>{hairstyle}</h2>
		{children}
	</>
	)
}

<Person>
	<h1>I am the children!</h1>
<Person/>
```
If there is nothing inside the component, children will return nothing.

### List:
- can't render objects in React
- map - creates a new array from calling a function for every array element.
- REMEMBER: objects are not valid returning
- Key prop typically it's going to be id.
- IN GENERAL: index key prop are bad to use and if you change or remove items will break your code. The best practice is to set a unique id.

### HINT: 
Before trying to create the logic, just try to render something in the screen.


### Events:
- The place where the function is, doesn't matter
- Very similar to vanilla JS.
- e.target
- e.preventDefault()      to forms
- You can onSubmit() in the form and button type equal to "submit" or you can onClick in the button.

### Mind Grenade:
-  Components are independent by default
-  It is much difficulty to do the same in Vanilla JS.

### Props Drill:
-  React data flow ( Up to Down )

### KEEP IN MIND:
-  When it comes to add a function that need arguments (i.e.: getBook(_id)) to a prop like onClick
```js
//This is not going to work because you are not //passing the arguments:
<Component onClick={getBook} />
```
```js
//This is not going to work because you are calling //instantly the function:
<Component onClick={getBook(2)} />
```
```js
//This is going to work:
<Component onClick={ () => getBook(2) } />
```

### Best practices to create a clean code:
-  Import and export between your JavaScript modules
-  The difference between "export" and "export default" is that "export" must be the same name, "export default" can be whatever the name you want
-  One of the best rules to organize your code is: When a component is only used for that file, keep in the same file, when it is used for multiple files, use in a separate file. Also, your intuition is important when it comes to readability. 

