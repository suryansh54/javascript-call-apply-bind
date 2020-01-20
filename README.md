# Javascript Call Apply Bind

You can use call()/apply() to invoke the function immediately. bind() returns a bound function that, when executed later, will have the correct context ("this") for calling the original function. So bind() can be used when the function needs to be called later in certain events when it's useful.

#### call() function example 01
```javascript
var obj = {name:"Suryansh"};

var greeting = function(a){
    return "Welcome "+this.name+" to "+a;
};

console.log(greeting.call(obj, "Japan"));
// returns output as Welcome Suryansh to Japan
```


#### apply() function example 01

```javascript
var obj = {name:"Suryansh"};

var greeting = function(a){
    return "Welcome "+this.name+" to "+a;
};

// array of arguments to the actual function
var args = ["Japan"];  
console.log(greeting.apply(obj,args));

// returns output as Welcome Suryansh to Japan
 ```
 
 #### bind --> bound() function example 01
 
 ```javascript
var obj = {name:"Suryansh"};

var greeting = function(a){
    return "Welcome "+this.name+" to "+a;
};

//creates a bound function that has same body and parameters 
var bound = greeting.bind(obj); 

console.log(bound("Japan")); //call the bound function

// returns output as Welcome Suryansh to Japan
 ```
