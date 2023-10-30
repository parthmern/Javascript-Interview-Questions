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

==================================================================

## 💜 Polyfills for MAP()
➔ how we can make function like map from scratch
```
Array.prototype.myMap = function (cb) {
    let temp = [];
     
    for(let i=0 ; i<this.length ; i++){           // this means ARRAY here
        temp.push(cb(this[i], i, this));
    }

    return temp;
}

const numbers = [1, 2, 3, 4, 5];
const doubledNumbers = numbers.myMap(function(number) {     //using myMap insted map func
  return number * 2;
});
console.log(doubledNumbers); // Output: [2, 4, 6, 8, 10]
```

## 💙 Polyfills for FILTER()
```
Array.prototype.myFilter = function (cb) {
    let temp = [];
     
    for(let i=0 ; i<this.length ; i++){           // this means ARRAY here
        if(cb(this[i], i, this)){
            temp.push(this[i]);
        }
    }

    return temp;
}
```

## 💚 Polyfills for REDUCE()
```
Array.prototype.myFilter = function (cb, initialValue) {
    var accuulator = initialValue;

    for(let i=0 ; i<this.length ; i++){
        accuulator = accuulator ? cb(accuulator,this[i],i,this) : this[i] ;
    }

    return accuulator;
}
```

============================================================================ <br />
➔ ✔️ map, filter, reduce allows CHAINING

## 🧡 difference between map vs forEach
➔ map returns array <br/>
➔ if map returns then we can add chain after it
```
const arr = [2, 5, 3, 4, 7];

const mapResult = arr.map((item)=>{
    return(item +2);                              // return new Array 
}).filter((itm)=>{                                // so we can do chaining
    return itm;      
});

arr.forEach((item)=>{
    console.log(item);
    // it cannot return anything        
    // so we cannot add chain
});
```

## Questions
```
let students = [
    {name: "pas", rollNum: 11, marks: 90},
    {name: "asas", rollNum: 54, marks: 30},
    {name: "hjfs", rollNum: 32, marks: 50},
    {name: "uii", rollNum: 55, marks: 20},
]

// QUE1- return only names of students in capital
const names= [];
for(let i=0; i<students.length; i++){
    names.push(students[i].name.toUpperCase());
}
// or
const Names = students.map((stu)=> stu.name.toUpperCase());

// QUE2- return the details of those students who scored more than 40 marks
const marks = students.filter((stu)=> stu.marks>40);

// QUE3- sum of marks of all students
const sum = students.reduce((acc, curr)=> acc+curr.marks ,0);

// QU4- return only the NAME of those students who scored more than 40 marks
const scoredName = students
                   .filter((stu)=> stu.marks>40)
                   .map((stu)=>stu.name);

// QUE5- return total marks of students with marks greater than 60 
//       after 20 marks have been added to those who scored less than 60

const ans = students
            .map((stu)=>{
                if(stu.marks<60){
                    stu.marks += 20 ;
                }
                return stu;
            })
            .filter((stu)=>stu.marks > 60)
            .reduce((acc, current)=> acc+curr.marks ,0);
```
