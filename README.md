Leroy
=====

> Css module monster for React className

Install
-------

```bash
npm install --save leroy
```

Getting Started
---------------

```javascript
import { leroy } from 'leroy'
import styles from './index.css'

class App extends React.Component {
	render() {
		return (
			<div
				className={leroy(styles).add('a', true)
					.add('b', false)
					.add('c', true).put()}
			/>
		)
	}
}
```

Usage
-----

```javascript
const styles = {
	a: "a1",
	b: "b2",
	c: "c3"
}

leroy(styles).add('a', true)
	.add('b', false)
	.add('c', true)
	.put();
// => 'a1 c3'

leroy(styles).bulk({
	a: true,
	b: false,
	c: true
}).put()
// => 'a1 c3'

leroy(styles).cls('a b').put()
// => 'a1 b2'
```