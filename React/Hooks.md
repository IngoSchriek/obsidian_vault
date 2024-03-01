### General Rules of Hooks:
- All the hooks need to start with "use".
- component must be uppercase
- the state must be inside the component body at the top level or inside your custom hooks
- don't call hooks conditionally (it is not allowed)
- set functions don't update state immediately

### Hooks:
- useState:
	- useState return an array of two elements, the initial value and the function.
	- every time you use the function "setSomething" will re-render the react app
	- group of multiple useState trigger the re-render only one time
	- if you have one object as a value in useState, and you want to update just one value inside the object, type:
	```[...object, key: updatedValue ]```
	- keep in mind that the code below doesn't work:
```jsx
const handleClick = () => {
    setValue(value + 1);
    //  be careful it's the old value
    console.log(value);
    //  so if you have any functionality
    // that relies on the latest value
    // it will be wrong !!!
  };
```
if you want that type of approach, react provide a way to do this. Use a function as an argument.
```jsx
const handleClick = () => {
	setValue((currentValue) => {
	const newValue = currentValue + 1
	return newValue
	})
}
```
Other case that you want to do it, is when it comes to use seTimeout():
```jsx
const handleClick = () => {
	setTimeout(() => {
	setValue((currentState) => {
	return currentState + 1
	}), 3000 })
	// The state will be changed instantly, based on
	// your clicks but will be trigger the re-render
	// only after the timeout
}
```
- useEffect:
	- first argument - callback function
	- second argument - dependency array
	- by default runs on each render (initial and re-render)
	- if dependency array empty [] runs only on initial render
	- don't setup the first argument as a async function
	- in the dependency array you can have multiple values and every time that value is going to change, the useEffect runs
	- very useful when it comes to use fetch(), example:
```jsx
const Component = () => {
	const [data, setData] = useState(null)
	useEffect(() => {
		const fetchData = async () => {
			const response = await fetch(url)
			const data = await response.json
			setData(data)
		}
		fetchData()
	}, [])
	if (!data) {
		return <h1>Loading...</h1>
	}
	return <div>{data}</div>
	
}
```
 CLEANUP FUNCTION:
 When using an interval inside a component that is rendered based in some condition ( like a dropdown button ) you will need to disable, clean, revert the process to untoggled. Example:
```jsx
const Component1 = () => {
	const [toggle, setToggle] = useState(false)
	return (
	<>
		{toggle & <Component2/>}
		<button onClick={setToggle(!toggle)}>Click to toggle</button>
	</>
	)	
}
const Component2 = () => {
	useEffect(() => {
	setInterval(() => {
	console.log('Hello world!')
	}, 1000)
	}, []) //will render every time is toggled
	return <h1>Hello world!</h1>
}
``` 
If you do this way, the setInterval will continue forever even if the component is not toggled, to fix that you need to useEffect return a cleanup function, like below:
```jsx
const Component2 = () => {
	useEffect(() => {
	const intId = setInterval(() => {
	console.log('Hello world!')
	}, 1000)
	return () => {
	cleanInterval(intId)
	}
	}, []) //will render every time is toggled
	return <h1>Hello world!</h1>
}
```
Always try to avoid using useEffect() by using its alternatives!!!!
- useRef: 
	- the simplest way to think about useRef is as a container
```jsx
const Compontent = () => {
	const refContainer = useRef(null)

	useEffect(() => {
	refContainer.current.focus()
	})
	return <input ref={refContainer}>
}
```

- useReducer:
	 - when it comes to useState, we pass a default state
	 - with useReducer we need to pass to things, a default state and a reducer (a function that is going to manipulate the state, called conventionally 'dispatch').
	 - multiple steps
	 - when it comes to useReducer or Redux lib, you wanna send (dispatch) something called 'action' and that action is gonna be handled in the 'reducer' and then whatever it gets returned in reducer is gonna be the new state
	 - in resume, reducer function get two things, state and an action
	 - to the action type, a convention is to use a constant string in upper case
```js
const CLEAR_LIST = 'CLEAR_LIST'
const RESET_LIST = 'RESET_LIST'
const REMOVE_ITEM = 'REMOVE_ITEM'
```

- useCallback:
	 - allows you to memoize a function
	 - It takes two arguments: the first is the function you want to memoize, and the second is an array of dependencies.
	 - The hook will return a memoized version of the function that only changes if one of the values in the dependency array changes.
	 - This can be useful in situations where you have an expensive function that you only want to recompute when its dependencies change.
```jsx
import React, { useCallback, useState } from 'react';

function MyComponent() {
  const [data, setData] = useState([]);
  const handleClick = useCallback(() => {
    console.log(data);
  }, [data]);

  return (
    <div>
      <button onClick={handleClick}>
        Click me
      </button>
    </div>
  );
}
```

- useMemo:
	- memoize a value that you will get back from the function
	- the first argue is a function that returns the value you want to memoize, and the second is an array of dependencies
	- very similar to useCallback 
```jsx
const value = useMemo(slowFunction, [])
  console.log(value)
```

- useTransition:
	- prevent the blocking of the UI
	- example:
```jsx
import { useState, useTransition } from 'react'

const LatestReact = () => {
  const [text, setText] = useState('')
  const [items, setItems] = useState([])
  const [isPending, startTransition] = useTransition()
  
  const handleChange = (e) => {
    setText(e.target.value)
    // slow down CPU
    startTransition(() => {
      const newItems = Array.from({ length: 5000 }, (_, index) => {
        return (
          <div key={index}>
            <img src="/vite.svg" alt="" />
          </div>
        )
      })
      setItems(newItems)
    })
  }
  return (
    <section>
      <form className="form">
        <input
          type="text"
          className="form-input"
          value={text}
          onChange={handleChange}
        />
      </form>
      <h4>Items Below</h4>
      {isPending ? (
        <h4>Loading...</h4>
      ) : (
        <div
          style={{
            display: 'grid',
            gridTemplateColumns: '1fr 1fr 1fr',
            marginTop: '2rem',
          }}
        >
          {items}
        </div>
      )}
    </section>
  )
}

export default LatestReact
```



### Custom Hooks
- same rules as regular hooks
- simplify component (less code)
- re-use functionality