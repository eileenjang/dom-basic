## execution context

##### 1. The execution context is created when code is executed, and code refers to global, function, eval, and module code.<br> 
##### 2. At this time, the execution context is managed by the stack.<br> 

```
console.log("it is global context.");

function func1(){
	console.log("it is func1.");
}

function func2(){
    func1();
    console.log("it is func2.");
}
func2();
```

```
it is global context.
it is func1.
it is func2.
```

##### global context -> global & func2 ->  global & func2 & func1 -> global & func2 -> global


## scope chain

```
var a = 1;
var b = 2;

function foo(){
	var a = 10;
  var b = 20;
  console.log(a + b); // 30
}

foo();
console.log(a + b); // 3
```

##### 1. The [[scope]] of the currently executing function object (foo function object). property of the currently executing function object. It contained a global variable object.
##### 2. In the variable object of the newly created foo execution context, the [[scope]] property of the newly created foo execution context's variable object with the [[scope]] value that we just copied,
##### 3. At the top of the list, we add a newly created variable object, which will be the variable object of the newly created foo execution context created by running the foo function.

![Gj5K5Qo](https://github.com/eileenjang/dom-basic/assets/82510378/0379e646-9dff-44d5-8353-e55ebe64afe5)

###### ref. https://chanhuiseok.github.io/posts/js-4/
