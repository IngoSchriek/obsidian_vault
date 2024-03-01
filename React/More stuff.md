### How to pass props to a component?
Let's say that you have a component like this:
```jsx
const DisplayNumber = () => {
	return <h1>1</h1>
}

const Table = () => {
	return (
	<div>
		<DisplayNumber />
		<DisplayNumber />
		<DisplayNumber />
	</div>
	)
}
```
And you want that each DisplayNumber component displays a different number like "1", "2", "3". If you leave it that way, the Table component will display three times 1. To fix that you will need to say the props you can pass to the DisplayNumber component.
```jsx
const DisplayNumber = ({ value }) => {
	return <h1>{value}</h1>
}

const Table = () => {
	return (
	<div>
		<DisplayNumber value=1 />
		<DisplayNumber value=2 />
		<DisplayNumber value=3 />
	</div>
	)
}
```
Don't forget to add to your ".eslintrc.cjs":
```json
 "react/prop-types": "off"
```

## But...
### You can pass values using another way, it is called CONTEXT API.

### Context API:
- Very useful when you have several nested components that you want to take a grandparent value and pass to a grandchild.
```jsx
// PARENT
import { useState, createContext } from 'react'

export const NavbarContext = createContext()

const Navbar = () => {
	const [user, setUser] = useState(null)

	return (
	// value={user} whatever you pass here, you can access at any child
	< NavbarContext.Provider value={{user, setUser}}>
	<UserContent />
	< NavbarContext.Provider />
	)
}
```
```jsx
// CHILD
import { useContext } from 'react'
import { NavbarContext } from "./Navbar"

const UserContent = () => {
	const { user, logout } = useContext(NavbarContext)

	return (
	<div>
		<h1>{user}</h1>
		<button onClick={logout}>Log out</button>
	</div>
	)
}
```

#### Other way with less lines of code (using custom hooks):
```jsx
// PARENT
import { useState, useContext, createContext } from 'react'

export const NavbarContext = createContext()

export const useAppContext = () => useContext(Navbar)

const Navbar = () => {
	const [user, setUser] = useState(null)

	return (
	// value={user} whatever you pass here, you can access at any child
	< NavbarContext.Provider value={{user, setUser}}>
	<UserContent />
	< NavbarContext.Provider />
	)
}
```
```jsx
// CHILD
import { useAppContext } from './Navbar'

const UserContent = () => {
	const { user, logout } = useAppContext
	return (
	<div>
		<h1>{user}</h1>
		<button onClick={logout}>Log out</button>
	</div>
	)
}
```

### Perfomance:
Every time a value is changed the parent is re-rendered, in some cases the parent may be render other components, or a lot of data, and that will cause a perfomance damage.
Tips:
- Always try to split the code in components to decrease the time of re-render of each components
- you can use memo(Component) function to optimize 
```jsx
const MyComponent = React.memo(function MyComponent(props) {
  /* render logic */
});
```
- useCallback hook
- best way to fetch data:
```jsx
const Component = () => {
	const fetchData = useCallback(() => {
		try {
		//...
		} catch {
		//...
		}
	}, [])
	useEffect(() => {
		fetchData()
	}, [fetchData])
}
```

### Suspense API:
example: 
```jsx
import { useState, useTransition, Suspense, lazy } from 'react'
const SlowComponent = lazy(() => import('./SlowComponent'))

///...
{show && (
  <Suspense fallback={<h4>Loading...</h4>}>
    <SlowComponent />
  </Suspense>
)}
```