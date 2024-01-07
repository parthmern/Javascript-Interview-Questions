## ❤️ Function Expression / definition / statement
➔ [chatGpt](https://chat.openai.com/share/6c7b3db0-713d-45c4-bfdd-fe318cf44a82)  
```
const multiply = function multiply(x, y) {
  return x * y;
};

console.log(multiply(4, 6)); // Output: 24
```

## 🧡 First class function
➔ when functions in that language are treated like any other variable. For example, in such a language, *a function can be passed as an argument to other functions*, can be returned by another function and can be assigned as a value to a variable. <br/>
➔ we can pass function inside another function just like variable.
```
function sayHello() {
  return "Hello, ";
}
function greeting(helloMessage, name) {
  console.log(helloMessage() + name);
}
// Pass `sayHello` as an argument to `greeting` function
greeting(sayHello, "JavaScript!");
// Hello, JavaScript!

```

## 💛 what is IIFI - ?
➔ Immediately Invoked Function Expression
```
(function () {
  // Your code here
})();

(function square(num){
    return(num*num)
})(5) 
```

## 💚 function scoped 
➔ [chatGpt](https://chat.openai.com/share/b5ee62e0-ff5e-435d-8192-4fb924911d43)  <br/>
➔ [que on chatGpt](https://chat.openai.com/share/c3bede02-b125-4fb6-a6df-9c9e7c9bedaa) <br/>

➔ [scopes](https://youtu.be/Uc6MJOL1Kio?si=f2QpcBcsebSdHD3S) <br/>

## 💙 Hoisting in function
