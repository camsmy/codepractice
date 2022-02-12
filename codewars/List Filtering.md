# Friend or Foe?

**Laguage used: Javascript**


### **Details:** ###
In this kata you will create a function that takes a list of non-negative integers and strings and returns a new list with the strings filtered out.

#### **Problems Encountered:** ###
* Restudy the use of isNaN and typeof
* unfamiliarity to forEach 
* avoid using a global variable

#### **Solution** ###
```
'use strict'
let array = [ 1, 2, '1', '123', 123];
function filter_list(l) {
  let result = [];
  l.forEach(item =>{
    if(typeof item !== 'string' && !isNaN(item)){ // typeof should use small letters, !isNaN=return true if item is numbers 
    result.push(item);
    }
  });
    return result;
}
filter_list(array);
```