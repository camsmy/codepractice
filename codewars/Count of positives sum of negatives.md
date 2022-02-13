# Count of positives / sum of negatives

**Laguage used: Javascript**


### **Details:** ###
Given an array of integers.

Return an array, where the first element is the count of positives numbers and the second element is sum of negative numbers. 0 is neither positive nor negative.

If the input array is empty or null, return an empty array.

Example
For input [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15], you should return [10, -65].

#### **Problems Encountered:** ###
* Struggle with forEach and shorthand if else 

#### **Solution** ###
```
'use strict'
function countPositivesSumNegatives(input) {
    let array = [0,0];

    if(input.length){//returns true if array is not empty: false if empty
        input.forEach(element => {
            let y = element > 0 ? array[0]++ : array[1] += element;
        });
    }
    return array;
}

let sample = [0, 2, 3, 0, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14];
console.log(countPositivesSumNegatives(sample));
```