#JavaScript
######1. split() splits a String bject into an array of strings
```JavaScript
var str = "How are you doing today?";
var res = str.split();      // ["How are you doing today?"]
var res = str.split("");    // ["H", "o", "w", " ", "a", "r", "e", " ", "y", "o", "u", " ", "d", "o", "i", "n", "g", " ", "t", "o", "d", "a", "y", "?"]
var res = str.split(" ",3); // ["How", "are", "you"]
var res = str.split("o");   // ["H", "w are y", "u d", "ing t", "day?"]
```
######2. reverse() reverses an array
```JavaScript
var myArray = ['one', 'two', 'three'];
myArray.reverse(); // ['three', 'two', 'one']
```

######3. join() joins all elements of an array into a string
```JavaScript
var a = ['Wind', 'Rain', 'Fire'];
a.join();      // 'Wind,Rain,Fire'
a.join(', ');  // 'Wind, Rain, Fire'
a.join(' + '); // 'Wind + Rain + Fire'
a.join('');    // 'WindRainFire'
```

######4. replace() replaces with a new string
```JavaScript
var str = "Visit Mom!";
var res = str.replace("Mom", "Dad");  // Visit Dad!

var myString = 'abc123.8<blah>';
myString = myString.replace(/\D/g,'');      // 1238

var myString = 'abc123.8<blah>';
myString = myString.replace(/[0-9]/g, '');  // abc.<blah>
```

######5. slice() returns the selected elements in an array, as a new array object or extracts parts of a string and returns the extracted parts in a new string
```JavaScript
var fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
var citrus = fruits.slice(1, 3);  // [Orange,Lemon]  beginning is inclued, end is excluded

var str = "Hello World";
var newStr = str.slice(1);  // "ello World"
```

######6. toLowerCase returns the calling string value converted to lowercase
```JavaScript
var str = "Hello World!";
var res = str.toLowerCase();  // hello world!
```

######7. toUpperCase() converts a string to uppercase letters
```JavaScript
var str = "Hello World!";
var res = str.toUpperCase();  // HELLO WORLD!
```

######8. substring() returns a subset of a string between one index and another, or through the end of the string
```JavaScript
var str = "Hello world!";
var res = str.substring(1, 4);  // ell - index 1, 2 and 3
```

######9. substr() extracts parts of a string, beginning at the character at the specified position, and returns the specified number of characters
```JavaScript
var str = "Hello world!";
var res = str.substr(1, 4);  // ello - index 1, 2, 3 and 4
```

######10. splice() modifies the content of an array by removing existing elements and/or adding new elements
```JavaScript
var myFish = ['angel', 'clown', 'mandarin', 'surgeon'];
var removed = myFish.splice(2, 0, 'drum');  
// removes 0 elements from index 2, and inserts 'drum'
// ['angel', 'clown', 'drum', 'mandarin', 'surgeon']
```

######11. indexOf() returns the position of the first occurrence of a specified value in a string
```JavaScript
var str = "Hello world, welcome to the universe.";
var n = str.indexOf("e");  // 1
```

######12 .filter() creates a new array with all elements that pass the test implemented by the provided function
```JavaScript
function isBigEnough(value) {
  return value >= 10;
}
var filtered = [12, 5, 8, 130, 44].filter(isBigEnough);  // [12, 130, 44]
```

######13. sort() sorts the elements of an array in place and returns the array
```JavaScript
var fruit = ['cherries', 'apples', 'bananas'];
fruit.sort();  // ['apples', 'bananas', 'cherries']

["z", "d", "g", "k"].sort(function compare(a, b) {
  // Compare "a" and "b" in some fashion, and return -1, 0, or 1
  // Less than 0: Sort "a" to be a lower index than "b"
  // Zero: "a" and "b" should be considered equal, and no sorting performed
  // Greater than 0: Sort "b" to be a lower index than "a"
})
```

######14. charAt() returns the character at the specified index in a string
```JavaScript
var str = "HELLO WORLD";
var res = str.charAt(0); // H
```

######15. fromCharCode() converts a Unicode number into a character
```JavaScript
var res = String.fromCharCode(65); // A
```

######16. charCodeAt() returns the Unicode of the character at the specified index in a string
```JavaScript
var str = "HELLO WORLD";
var n = str.charCodeAt(0); // 72
```

######17. parseInt() parses a string and returns an integer of the specified radix
```JavaScript
var a = parseInt("10")  // 10
var b = parseInt("1111", 2) // 15
```

######18. Math.round() round a number to the nearest integer
```JavaScript
Math.round(2.5);  // 3
```

######19. Math.floor() round a number downward to its nearest integer
```JavaScript
Math.floor(1.6);  // 1
```

######20. Math.max() returns the largest of zero or more numbers
```JavaScript
Math.max(10, 20);  // 20
```

######21. Math.min() returns the smallest of zero or more numbers
```JavaScript
Math.min(10, 20);  // 10
```

######22. reduce() applies a function against an accumulator and each value of the array to reduce it to a single value
```JavaScript
var total = [0, 1, 2, 3].reduce(function(acc, cur) { // acc represents accumulated value, cur represents current item
  return acc + cur;
}, 0);  //  0 + 0, 0 + 1, 1 + 2, 3 + 3 = 6
```

######23. repeat() returns a new string which contains the specified number of copies of the original string
```JavaScript
var name = "kevin".repeat(3);  // kevinkevinkevin
```

######24. Object.keys() returns an array of a given object's own enumerable properties
```JavaScript
var obj = { "a": 1, "b": 2 };
Object.keys(obj);  // ["a", "b"]
```

######24. test() tests for a match in a string
```JavaScript
var str = "Hello world!";
var patt = /Hello/g;
var result = patt.test(str); // true
```

######24. forEach() executes a provided function once per array element
```JavaScript
function logArray(element) {
    console.log(element);
}
[1, 2, 3, 4, 5].forEach(logArray);  // 1 2 3 4 5
```

######25. map() creates a new array with the results of calling a provided function on every element in this array
```JavaScript
function sayHi(jedi, index) {
    if (jedi === "Obi Wan Kenobi") {
        return "And last but not less important, I'm #" + (index + 1) + " " + jedi;
    }
    else {
        return "My name is " + jedi + ", I'm #" + (index + 1);
    }
}
var jediMasters = ["Leia", "Anakin", "Luke", "Obi Wan Kenobi"];
var jediMastersSayHi = jediMasters.map(sayHi);
// ["My name is Leia, I'm #1", "My name is Anakin, I'm #2", "My name is Luke, I'm #3", "And last but not less important, I'm #4 Obi Wan Kenobi"]
```

######26. shift() removes the first element from an array and returns that element
```JavaScript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var firstElement = fruits.shift();
// fruits = ["Orange", "Apple", "Mango"] ; firstElement = "Banana";
```

######27. pop() removes the last element from an array and returns that element
```JavaScript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var lastElement = fruits.pop();
// fruits = ["Banana", "Orange", "Apple"] ; lastElement = "Mango";
```

######28. Number() converts the object argument to a number that represents the object's value
```JavaScript
Number("123")  // 123
```

######29. eval() function evaluates or executes an argument
```JavaScript 
eval("2 + 2")  // 4; eval takes string as argument
```

######30. setInterval() method calls a function at specified intervals (in milliseconds)
```JavaScript 
setTimeout(function(){
  alert("Hello");
}, 3000);
```
