---
title: Nine Super Useful Javascript Tips Property Selectors
date: 2023-08-05 08:14:48

categories:

  - javascript
  
tags:
  - javascript
  - code snippets
  - program
  - JavaScript tips
  
description: Nine Super Useful Javascript Tips Property Selectors,Make your programming skills more accessible.

cover: https://s2.loli.net/2023/09/23/snhiB9vfQlMzSj6.png

---
## Preface

In the process of actual development work, I have accumulated some common and super useful Javascript tricks and code snippets, including other great compilation of JS tips.

Today's article, I carefully filtered 9 I think more practical skills to share with you, you are also welcome to leave us a message in the comments section, you think some important and useful skills to share with you.

### 1. Dynamic loading of JS files

In some special scenarios, especially in the development of some `libraries` and `frameworks`, we will sometimes dynamically load and execute JS files.
The following is a simple package using Promise.

```javascript
function loadJS(files, done) {
   // Get the head tag
   const head = document.getElementsByTagName('head')[0];
   Promise.all(files.map(file => {
     return new Promise(resolve => {
       // create script tag and add to head
       const s = document.createElement('script');
       s.type = "text/javascript";
       s.async = true;
       s.src = file;
       // Listen to the load event, resolve if the loading is complete
       s.addEventListener('load', (e) => resolve(), false);
       head.appendChild(s);
     });
   })).then(done); // everything is done, execute the user's callback event
}
loadJS(["test1.js", "test2.js"], () => {
   // user's callback logic
});
```
There are two core points in the code above. One is to use Promise to process asynchronous logic, but to use script tags to load and execute js.

### 2. Implementing the template engine

The following example uses very little code to implement a `dynamic template rendering engine`. It not only supports normal dynamic variable substitution, but also supports dynamic JS syntax logic including for loops, if-judgments and so on.

```javascript
// This is a dynamic template that contains js code
var template =
'My avorite sports:' +
'<%if(this.showSports) {%>' +
     '<% for(var index in this.sports) { %>' +
     '<a><%this.sports[index]%></a>' +
     '<%}%>' +
'<%} else {%>' +
     '<p>none</p>' +
'<%}%>';
// This is the function string we're going to concatenate
const code = `with(obj) {
   var r=[];
   r.push("My avorite sports:");
   if(this. showSports) {
     for(var index in this. sports) {
       r. push("<a>");
       r.push(this.sports[index]);
       r. push("</a>");
     }
   } else {
     r.push("<span>none</span>");
   }
   return r.join("");
}`
// dynamically rendered data
const options = {
   sports: ["swimming", "basketball", "football"],
   showSports: true
}
// Build a feasible function and pass in parameters to change the direction of this when the function is executed
result = new Function("obj", code).apply(options, [options]);
console.log(result);
```

### 3. Using reduce to convert data structures

Sometimes the `front-end` needs to be converted to the data coming from the back-end to adapt to the front-end business logic, or to convert the data format of the component and then pass it to the back-end processing, and reduce is a very powerful tool.

```javascript
const arr = [
    { classId: "1", name: "Jack", age: 16 },
    { classId: "1", name: "Jon", age: 15 },
    { classId: "2", name: "Jenny", age: 16 },
    { classId: "3", name: "Jim", age: 15 },
    { classId: "2", name: "Zoe", age: 16 }
];
groupArrayByKey(arr, "classId");

function groupArrayByKey(arr = [], key) {
    return arr.reduce((t, v) => (!t[v[key]] && (t[v[key]] = []), t[v[key]].push(v), t), {})
}
```

A lot of complex logic is very simple if handled by reduce.

### 4. Adding default values

Sometimes, `methods` require the user to pass in parameters. Usually, we have two ways to handle this. If the user doesn't pass it in, we usually give a default value, or the user must pass in a parameter, and if they don't, an error is thrown.

```javascript
function double() {
     return value * 2
}
// If not passed, give a default value of 0
function double(value = 0) {
     return value * 2
}
// The user must pass a parameter, and an error will be thrown if no parameter is passed
const required = () => {
     throw new Error("This function requires one parameter.")
}
function double(value = required()) {
     return value * 2
}
double(3) // 6
double() // throw Error
```
The Listen method is used to create a NodeJS native http service and listen to the port, create the context in the service's callback function, and then call the callback function registered by the user and pass the generated context. Let's look at the previous implementations of createContext and handleRequest.

### 5. The function is executed only once

In some cases, we have special `scenarios` where a function is only allowed to execute once, or a binding method is only allowed to execute once.

```javascript
export function once (fn) {
   // Use the closure to determine whether the function has been executed
   let called = false
   return function () {
     if (! called) {
       called = true
       fn.apply(this, arguments)
     }
   }
}
```

### 6. Implementing Curry

`Currying` in JavaScript is the process of converting a function that takes multiple arguments into a series of functions that take only one argument. This allows for more flexible use of functions, reduces code repetition, and improves code readability.

```javascript
function curry(fn) {
  return function curried(...args) {
    if (args.length >= fn.length) {
      return fn.apply(this, args);
    } else {
      return function(...args2) {
        return curried.apply(this, args.concat(args2));
      };
    }
  };
}

function add(x, y) {
  return x + y;
}

const curriedAdd = curry(add);

console.log(curriedAdd(1)(2)); // output 3
console.log(curriedAdd(1, 2)); // output 3
```
### 7. Implementing the singleton pattern

JavaScript's `singleton pattern` is a commonly used design pattern. It ensures that there is only one instance of a class and provides a global access point to that instance. It has a wide range of application scenarios in JS, such as shopping carts, cached objects, global state management, and so on.

```javascript
let cache;

class A {
  // ...
}

function getInstance() {
  if (cache) return cache;
  return (cache = new A());
}

const x = getInstance();
const y = getInstance();

console.log(x === y); // true
```
### 8. Implementing the CommonJs specification

The core idea of the CommonJS specification is to treat each file as a module, and each module has its own scope in which variables, functions, and objects are private and inaccessible from the outside. To access the data in a module, you must `export` and `request`.

```javascript
// id: full file name
const path = require('path');
const fs = require('fs');

function Module(id){
     // Used to uniquely identify the module
     this.id = id;
     // Properties and methods used to export modules
     this.exports = {};
}

function myRequire(filePath) {
     return Module._load(filePath);
}

Module._cache = {};

Module._load = function(filePath) {
      const realPath = Module._resolveFilename(filePath);
     let cacheModule = Module._cache[realPath];
     if(cacheModule) return cacheModule.exports;
     let module = new Module(realPath);
     module.load(realPath);
     return module.exports;
}

// The node file is not discussed yet
Module._extensions = {
    // Process the js file
   ".js": handleJS,
   // process the json file
   ".json": handleJSON
}

function handleJSON(module) {
   const json = fs.readFileSync(module.id, 'utf-8')
   module.exports = JSON.parse(json)
}

function handleJS(module) {
   const js = fs.readFileSync(module.id, 'utf-8')
   let fn = new Function('exports', 'myRequire', 'module', '__filename', '__dirname', js)
   let exports = module.exports;
   fn.call(exports, exports, myRequire, module, module.id, path.dirname(module.id))
}

Module._resolveFilename = function (filePath) {
   let absPath = path.resolve(__dirname, filePath);
   let exists = fs.existsSync(absPath);
   if (exists) return absPath;
   let keys = Object.keys(Module._extensions);
   for (let i = 0; i < keys.length; i++) {
     let currentPath = absPath + keys[i];
     if (fs.existsSync(currentPath)) return currentPath;
   }
};

Module.prototype.load = function(realPath) {
   // Get the file extension and hand it over to the corresponding method for processing
   let extname = path.extname(realPath)
   Module._extensions[extname](this)
}
```

The above is a simple implementation of the CommonJs specification. The core solves the isolation of scopes and provides the Myrequire method to load methods and properties.

### 9. Recursive acquisition of object properties

If I had to choose the most widely used design pattern, I would choose the Observer pattern. If I had to pick the algorithmic thinking I've encountered the most, it would be recursion. Recursion divides the original problem into structures that have the same structure. `Subproblems` are then solved in turn, and the results of the subproblems are combined to finally get the answer to the original problem.

```javascript
const user = {
   info: {
     name: "Jacky",
     address: { home: "MLB", company: "AI" },
   },
};

// obj is the object to get the property, path is the path, and fallback is the default value
function get(obj, path, fallback) {
   const parts = path.split(".");
   const key = parts.shift();
   if (typeof obj[key] !== "undefined") {
     return parts.length > 0 ?
       get(obj[key], parts.join("."), fallback) :
       obj[key];
   }
   // return fallback if key not found
   return fallback;
}

console.log(get(user, "info.name")); // Jacky
console.log(get(user, "info.address.home")); // MLB
console.log(get(user, "info.address.company")); // AI
console.log(get(user, "info.address.abc", "fallback")); // fallback
```

## Summary
This is all I have selected for you today, and 9 JavaScript tips that I think are more useful, I hope it will help you.

## Related areas of expansion: (Technology Frontiers)

A Riposte! Regarding the fact that low-code is currently active in the tech world!

What is low-code? A set of digital technology tool platforms that enable rapid building, data orchestration, connectivity ecosystems, and middle-office services based on graphical drag-and-drop, parameterized configuration, and other more efficient ways. It realizes scenario application innovation in digital transformation with little or no code. It can alleviate or even solve the huge market demand and traditional development productivity caused by the contradiction between supply and demand, is the digital transformation process under the trend of cost reduction and efficiency.

This side introduces a good low-code platform - JNPF rapid development platform. In recent years, it has been more outstanding in terms of market performance and product competitiveness, and adopts the latest mainstream front-back separation framework (SpringBoot+Mybatis-plus+Ant-Design+Vue3). The code generator has low dependency and flexible expansion capability, which can flexibly realize secondary development.

JNPF as a representative of the enterprise-level low-code platform in order to support higher technical requirements of application development , from database modeling , Web API construction to page design , and traditional software development is almost no difference , just through the low-code visualization model , reducing the construction of "add, delete, change, and check" function of the duplication of labor , have not understood the low-code partners can try to understand low-code partners can try to understand.




