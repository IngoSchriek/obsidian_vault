### Controlled Inputs:
When you hear about controlled inputs, just think about there is going to be a state value, that can be one value or each input has its own value.
Basically whatever you type, will be added to the state value and when you submit the form, you can just grab this state value.

### JavaScript Dynamic Object Keys:
```js
// dot notation
const person = {
  name: 'john'
}
console.log(person.name)

// square bracket notation
const items = {
  'featured-items': ['item1', 'item2']
}
console.log(items['featured-items'])
console.log(person.name)

let appState = 'loading';

const app = {
  [appState]: true
}

console.log(app) // output: {loading: true}
```

### Multiple Inputs:
```jsx
/// ... Update a object with multiple values of multiple inputs
useState({ ...user, [e.target.name]:e.target.value })
```

### Other Inputs:
```jsx
///....
<select name="framework" id="framework" value={framework} onChange={handleFramework}>
	{frameworks.map((framework) => {
		return <option key={framework}>{framework}</option>})}
</select>
///...
```

### FormData API:
```jsx
  const handleSubmit = (e) => {
    e.preventDefault();
    const formData = new FormData(e.currentTarget)
    // console.log(formData)
    // const email = formData.get('email')
    // console.log([...formData.entries()])
    const newUser = Object.fromEntries(formData)
    // console.log(newUser)
    setValue(value + 1)
    e.currentTarget.reset()
  };
```
