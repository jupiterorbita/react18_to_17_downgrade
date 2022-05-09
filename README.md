# Downgrade React 18 to 17

in your ```package.json``` **replace**:

```json
"react": "^18.0.0"
"react-dom": "^18.0.0"
```

with

```json
"react": "^17.0.2"
"react-dom": "^17.0.2"
```

Then go to your entry file `index.js` At the top, **replace**:

```js
import ReactDOM from 'react-dom/client'
```

with

```js
import ReactDOM from 'react-dom';
```

Still in your `index.js` file, **replace**:

```js
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

with

```js
ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root')
);
```

**Delete** your `/node_modules` and run `npm install`
After installation, run `npm start`
Enjoy 😊

[source](https://stackoverflow.com/questions/46566830/how-to-use-create-react-app-with-an-older-react-version "Stack-overflow")
