# CSS Styles in React

First we need to import css file in `React`

```js
import './index.css'
```

now we can just write our css like normal

```css
/* src/index.css */
h1 {
  color: green;
  font-style: italic;
}
```

we can set up class for element in `React` by using `className`

```js
<li className='note'>
    {note.content} 
    <button onClick={toggleImportance}>{label}</button>
</li>
```

you can also use inline styles if u want to

```js
const Footer = () => {
  const footerStyle = {
    color: 'green',
    fontStyle: 'italic',
    fontSize: 16
  }
  return (
    <div style={footerStyle}>
      <br />
      <em>Note app, Department of Computer Science, University of Helsinki 2022</em>
    </div>
  )
}

export default Footer
```