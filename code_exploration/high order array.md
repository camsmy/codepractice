#Combination of filter and map

```
'use strict'
const todos = [
    {
        id: 1,
        text: 'take out trash',
        isCompleted: true
    },
    {
        id: 2,
        text: 'Do assignmenmt',
        isCompleted: true
    },
    {
        id: 3,
        text: 'do some codewars',
        isCompleted: false
    },
];

const array = [1,2,3,4,5,5,'sasfda','kaka']

const todotext = todos.filter(el =>{
    return el.isCompleted === true;
}).map(index => {
    return index.text;
})
console.log(todotext);
```