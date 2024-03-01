### Now you will learn:
- [[Hooks]]: useState, useEffect, useRef, useContext, useReducer, etc.
- [[Forms]]: controlled/uncontrolled inputs, value, onChange, FormData API
- [[More stuff]]: Context API, prop drilling, custom hooks, perfomance, etc.

### Render and Re-render:
Render happens with the first load or when the root component is first rendered.
Re-render happens when the state or the props of a component change.

Remember: map() and filter() methods are very useful!!!

### Project Structure:
Normally somewhere in the src:
/components/componentName.jsx
But as the project grows, you will need a better structure like:
- create a Navbar folder
	- setup Navbar.jsx (component)
	- Navbar.css (styles)
- import in App.jsx 
```jsx
import Navbar from 'pathToFile/Navbar/Navbar';
```
- To don't repeat the name of the component you can create an index.jsx file inside the component file and just put the content from Navbar.jsx inside, or put the code below inside:
```jsx
export { default } from './Navbar'
```
When talking about pages, and pages in React is components, you will want to make a jsx file for each page/component and then import and export at the index.jsx.
```jsx
//index.jsx
import Home from "PathToFile/Home"
import About from "PathToFile/About"
import Services from "PathToFile/Services"

export { Home, About, Services }

//App.jsx
import { Home, About, Services } from "PathToFolder"
```
You can also export a group of components (check the tutorial for this one), but keep in mind that you will use this kind of folder structure only with some projects. If you want, you can install the extension glean in Visual Studio Code to help you.


