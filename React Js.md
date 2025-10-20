Open source, for UI, not a frameworks
created by facebook
-component based
-reusable code
-declarative - tell react whta you want and react will build the UI for you

Javascript :
this
map
filter
reduce

let
const
arrow functions
template literals
default parameters
object literals
rest and spread
destructing assignment

2 ways to create react app
1.npx create-react-app helloworld : npm package runner

2.npm install create-react-app -g
create-react-app helloworld

package.json : dependencies, name version
node modules : folder where dependencies are installed
public : index.html : only html files, only 1 div tag, as SPA
src : 
starting point of application is index.js, we specify the root component there, which is App component and the DOM element which will be controlled by react, DOm element with ID - root
App.js : html

index.html -> index.js -> App.js
when you run the command -npm start, index.html is served in the browser, index.html contains the root DOM node. next it enters index.js -ReactDOM renders the App component on the the root DOM node, App component  contains html which is rendered on root DOM node

Component:
part of UI, reusable , can contain other components eg. App contains other component,
Component is placed in js file
2 types
![[Pasted image 20251020173339.png]]
Functional Components
takes props as input and returns HTML as ouput