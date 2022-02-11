# Friend or Foe?
### **Details:** ###
- - - -
Make a program that filters a list of strings and returns a list with only your friends name in it.

If a name has exactly 4 letters in it, you can be sure that it has to be a friend of yours! Otherwise, you can be sure he's not...

Ex: Input = ["Ryan", "Kieran", "Jason", "Yous"], Output = ["Ryan", "Yous"]

i.e.

friend ["Ryan", "Kieran", "Mark"] `shouldBe` ["Ryan", "Mark"]
Note: keep the original order of the names in the output.

#### **Problems Encountered:** ###
- - - -
* Test case includes a ['Ryan', 'Marks', '123', '1'].
* No repeating names in the returned array

#### **Solution** ###
- - - -
```
'use strict'
let input = [ 'Ryan', 'Mark', 'Ryan'];
let myfriends = [];

function friend(friends){
  friends.forEach(item => {
    if(item.length <= 4 && isNaN(item)){//isNaN is used here to check if a string is a number (bullet 1)
        myfriends.push(item);
    }
  })
}

friend(input);
let newfriends = [...new Set(myfriends)]; // ES6 solution to remove the duplicates in an array
console.log(newfriends);
```