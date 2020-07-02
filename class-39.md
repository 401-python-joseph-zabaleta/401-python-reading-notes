# Reading Notes 39  

## Articles  

### React Router  
* [Link to Article](https://reacttraining.com/react-router/web/guides/quick-start)  

### React - Styling FAQ  
* [Link to Article](https://reactjs.org/docs/faq-styling.html)  

Styling and CSS:  

- You can pass a string as the `className` prop:  
```js
render() {
  return <span className="menu navigation-menu">Menu</span>
}
```
- You can use inline styles if you wish  
- CSS classes are generally better for performance than inline styles  
- There is a `CSS-in-JS` concept that allows you to write CSS rules in JS. However this is not provided by React and is provided by third parties.  

### NextJs  
* [Link to Article](https://nextjs.org/learn/basics/create-nextjs-app)  

NextJS: The React Framework. 

The initial creation of a NextJS app is similiar to a ReactApp:
- `npm init next-app ` which under the hood is calling `create-next-app`  

#### Pages in Next.js
- A page is a React Component exported from a file in the `pages` directory.  
- Pages are associated with a route based on their file name.  

#### Navigation Between Pages  
- Link Components  
    - When linking with pages you generally use an anchor tag `<a>`.  
    - In Next.js you use the `<Link>` tag.  
    - Import `Link` component from `next/link`  

#### Summary  
Next.js automatically optimizes your application for the best performance by:  
- Code splitting  
- Client-side Navigation  
- Prefetching (in production)  

You create routes as files under `pages` and use the built-in `Link` component. No routing libraries are required.  

## Bookmark/Skim 
* [Sass](https://sass-lang.com/guide)  
* [Sass Cheatsheet](https://devhints.io/sass)  