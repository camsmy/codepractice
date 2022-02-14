# Calculate average

**Laguage used: Javascript**


### **Details:** ###
Write a function which calculates the average of the numbers in a given list.

Note: Empty arrays should return 0.

#### **Problems Encountered:** ###

#### **Solution** ###
```
'use strict'
function find_average(array) {
    let  sum=0;
    if (array.length === 0){
        return 0
    }else{
      array.forEach(element => {
          sum+=element;
      });
   }
   return sum/array.length;
}
```