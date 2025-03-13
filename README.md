# 30-Days-of-Javascript-Problem-Solving-
# Problem statement :
Write a function ```createHelloWorld```. It should return a new function that always returns *Hello World*.

# Solution
```js
var createHelloWorld = function (){
 return (...args)=>"Hello World"
};

// "Hello World"
```


# Explanation: Understanding  what is Closure is required to solve this problem?
In programming: the Closure is the combination of functions and  its lexical environment. In which variables that are declared in side a function will be accessable to  inside of that declared function and also any nested function can *Remember* their outer function variable this is called *lexical scoping* 

```js
function outer(){
const name = "Bob";

function inner(){

console.log(`Hello ${name}!`);
}
return inner()
}
const greeating = outer();
greeating();
```
