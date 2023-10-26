## 💙 Array.map()
➔ it will return new array - [chatGpt](https://chat.openai.com/share/b6ec49b1-cc81-4106-b321-56d93484e159)
```
const numbers = [1, 2, 3, 4, 5];

// Using map to create a new array with each element doubled
const doubledNumbers = numbers.map(function(number) {
  return number * 2;
});

console.log(doubledNumbers); // Output: [2, 4, 6, 8, 10]
```

## 🧡 Array.filter()
➔ it will return new array whose elemets fullfill the condition - [chatGpt](https://chat.openai.com/share/2e14eaea-a5b7-42a9-88d5-772a1e687c9d)
```
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

// Filter even numbers
const evenNumbers = numbers.filter(function (element) {
  return element % 2 === 0;
});

console.log(evenNumbers); // Output: [2, 4, 6, 8, 10]
```

## 💛 Array.reduce()
➔ accumulate value - [chatgpt](https://chat.openai.com/share/ab5dcc90-88d1-40f8-bae7-3a5c05aea056)
```
const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((accumulator, currentValue) => {
  return accumulator + currentValue;
}, 0); // 0 is the initial value for the accumulator

console.log(sum); // Output will be 15 (1 + 2 + 3 + 4 + 5)
```
