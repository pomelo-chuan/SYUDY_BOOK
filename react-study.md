react
---

#### JSX

```javascript
// 这个就是JSX
const element = <h1>Hello World!</h1>
```

```jabascript
// JSX可以在{单大括号中}嵌入javascript语句：
function formateName(name) {
	return name.firstName + ' ' +  name.lastName;
}

const name = {
	firstName: 'Harper',
	name.lastName: 'Perez'
};

const element = (
	<h1>
		Hello {formateName(name)}!
	</h1>
);

ReactDom.render(
element,
document.getElementById('root')
);
```

#### component and props

1. 函数式组件
```javascript
// The simplest way to define a component is to write a JavaScript function:
function welcome(props) {
	return <h1>Hello, {props.name}</h1>
}
```

