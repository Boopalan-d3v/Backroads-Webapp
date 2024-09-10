Checkout below link

# Backroads App

https://backroads-w3b.netlify.app/

#### Create New React App

- install

```sh
npx create-react-app@latest backroads-app
```

- run dev server

```sh
npm start
```

#### SRC Folder (boilerplate)

- index.js

```js
import React from 'react'
import ReactDOM from 'react-dom/client'

// styles (typically global)
import './index.css'

// convention to name it App and setup in a separate file
import App from './App'
// import report web vitals
import reportWebVitals from './reportWebVitals'

// StrictMode

// StrictMode is a tool for highlighting potential problems in an application.Activates additional checks and warnings for its descendants.Runs only in Development, does not impact the production build. RENDERS TWICE !!! Possible to remove.

const root = ReactDOM.createRoot(document.getElementById('root'))
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
)

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals()
```

- remove in src

  - setupTests.js
  - reportWebVitals.js
  - App.test.js


App.js

```js
function App() {
  return <h1>backroads app</h1>
}

export default App
```

- remove
  - remove logo.svg
  - App.css

#### Setup Structure

- public/index.html

  - change title
  - copy/paste font-awesome link (from html project)

- index.css

  - copy/paste css (from html project - css/styles.css)
  - error in line 209, just comment out for now

```css
@media screen and (min-width: 768px) {
  /* .hero {
    background: linear-gradient(rgb(44, 174, 186, 0.7), rgba(0, 0, 0, 0.7)),
      url('../images/main.jpeg') center/cover no-repeat;
  } */
}
```

- src folder
  - copy/paste images folder (from html project)
  - move favicon.ico to public
- App.js
  - refactor to <React.Fragment>
  - copy/paste all the content within body tags, up to <script> (index.html)
  - select all "class" instances and refactor to "className" (CMD + D)
  - fix the comment bug (remove or comment out)
  - don't worry about - Using target="\_blank" without rel="noreferrer" warning,
    will fix it later
  - move README.md from final to current project

#### Setup Components

- in src create components folder
- in the components create following files
  - Navbar.js
  - Hero.js
  - About.js
  - Services.js
  - Tours.j
  - Footer.js
- setup components with default export (snippet - rafce)
- carefully move the code from App.js into components (files)
- App.js should be empty
- import and render all components in App.js 


#### Smooth Scroll

- html/css feature

```html
<!-- link -->
<a href="#services"> services </a>
<!-- element -->
<section id="services"></section>
```

```css
html {
  scroll-behavior: smooth;
}
.section {
  /* navbar height */
  scroll-margin-top: 4rem;
}
```




#### Continuous Deployment

- fix warnings (About Section)

- netlify account
- github account
- basic git commands :

  - remove existing git repo
    - Mac : rm -rf .git
    - Windows : rmdir -Force -Recurse .git
    - Windows : rd /s /q .git
      Windows commands were shared by students and I have not personally tested them.
  - setup new repo
    - git init
      create an empty git repository
    - git add
      adds new or changed files in your working directory
      to the Git staging area
    - git add .
      adds entire project
      apart from files/directories specified in .gitignore
    - git commit -m "first commit"
      A shortcut command that immediately creates a commit
      with a passed commit message.
    - push to github
      git remote add origin git@github.com:your-profile/repo-name.git
      git branch -M main
      git push -u origin main


#### Warnings

- Netlify treats warnings as errors

package.json

```json
"scripts": {
    "start": "react-scripts start",
    "build": "CI= react-scripts build",
    "local-build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  },
```
