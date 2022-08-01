# Components
- reusable blocks, provides
	- Re-usability
	- Separation of concerns
	- are function that return HTML code.

```jsx
ReactDom.createRoot(document.getElementById(""))
	.render(<Component />);
```
- Inject the react component into the HTML.

# JSX (javascript xml)

```jsx
function App() {
	return (
		<div> 
			<h1> App  </h1>
			<ChildComponent />	
		</div>	
	);
}

function ChildComponent() {
	return <section/>
}
```
- Custom components must begin with Capital letters
- A Component must have only **one root component**.

## Styling

 1. By directly Importing css file into the component file.
 ```jsx
 import "style.css";
 
 const component = () => <div className="component"></div>
```

## JSX Expressions

```jsx
	<div> {expression} </div>
```

- Any code inside a curly brace is computed and injected to the rest of HTML code in jsx as long as the item returned is string and not any other object.

```jsx
	return (
		<div>
			<h1> Title </h1>
			<ChildComponent data={APIResult}/>
		</div>
	)
``` 

```jsx
	return React.createElement(
		'div', 
		{}, 
		React.createElement('h1', 'Title'),
		React.createElement(ChildComponent, {data: APIResult}));
```
## Props/Custom Attributes

- Objects pass to the components as a parameter where the properties are those passed as custom attributes to the component.
```jsx
function Component(props){
	return <h1> Hello {props.name}!</h2>;
}


<Components name={"Dagem Tadesse"} />
```

## Passing Children

- props object also contains children property(reserved) which could be use to nest components.
```jsx
function Wrapper(props){
	return <div className="Wrapper">{props.children}</div>
}

<Wrapper>
	<h2> Tittle </h2>
</Wrapper>
```
