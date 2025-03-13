# 30-Days-of-Javascript-Problem-Solving
# Problem statement No. 1 :
Write a function ```createHelloWorld```. It should return a new function that always returns *Hello World*.

# Solution 1
```js
var createHelloWorld = function (){
 return (...args)=>"Hello World"
};

// "Hello World"
```


# Explanation: Understanding  what is Closure?  required to solve this problem?
In programming: the Closure is the combination of functions and  its lexical environment. In which variables that are declared in side a function will be accessable to  inside of that declared function and also any nested function can *Remember* their outer function variable this is called *lexical scoping* 

```js
function outer(){
const name = "Bob";

function inner(){
console.log(`Hello ${name}!`);
}

return inner
}
const greeating = outer();
greeating();
```

# Solution 2
```js
const createHelloWorld = function (){
const greeting = "Hello World";

return function (){
return greeting
 };
}
```
# Problem statement No. 2 :
Write a program that returns the factorials of a number let say 3 using ```function expression``` of javascript 

# Solution 1
```js
const factorials = function fact(n){
return n < 2 ? 1 : n * fact(n-1)
}
console.log(factorials(3))
```
# Explanation (factorials & function expression ):
In mathematics the factorial of a non-negative integer number ```n``` are denoted by 
n!{\displaystyle n!} is the product of all positive integers less than equal to ```n``` with the next smaller factorial like in the above solution factorials function returns
the ```n < 2 ? 1 ``` ensure that the number given is not a negative integer and then the ```n * fact(n-1)``` ensure the given number is being multiplied by their next smaller in this case which is  ```fact(3-1)``` 2  and the given number is 3.

# Function expression
A ```function expression``` is almost same as syntactically as ```function declaration``` but the difference between ```function declaration``` and ```function expression``` is that the ```function declaration``` having function name while in the ```function expression``` it is omitted. A function expression can be used as IIFE(Immediately Invoked Function Expression) it is invoked as soon as it is defined 

# Example
```js
const expression = function (number){
return number * number
};
console.log(expression(4)) //16
```





