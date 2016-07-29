#JavaScript
######1. split() splits a String bject into an array of strings
```JavaScript
var str = "How are you doing today?";
var res = str.split();      //["How are you doing today?"]
var res = str.split("");    //["H", "o", "w", " ", "a", "r", "e", " ", "y", "o", "u", " ", "d", "o", "i", "n", "g", " ", "t", "o", "d", "a", "y", "?"]
var res = str.split(" ",3); //["How", "are", "you"]
var res = str.split("o");   //["H", "w are y", "u d", "ing t", "day?"]
```
######2. reverse() reverses an array
```JavaScript
var myArray = ['one', 'two', 'three'];
myArray.reverse(); // ['three', 'two', 'one']
```

######3. join() joins all elements of an array into a string
```JavaScript
var a = ['Wind', 'Rain', 'Fire'];
a.join();      //'Wind,Rain,Fire'
a.join(', ');  //'Wind, Rain, Fire'
a.join(' + '); //'Wind + Rain + Fire'
a.join('');    //'WindRainFire'
```

######4. replace() replaces with a new string
```JavaScript
var str = "Visit Mom!";
var res = str.replace("Mom", "Dad");  //Visit Dad!

var myString = 'abc123.8<blah>';
myString = myString.replace(/\D/g,'');      //1238

var myString = 'abc123.8<blah>';
myString = myString.replace(/[0-9]/g, '');  //abc.<blah>
```

######5. slice() returns the selected elements in an array, as a new array object
```JavaScript
var fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
var citrus = fruits.slice(1, 3);  //Orange,Lemon
```

######6. toLowerCase returns the calling string value converted to lowercase
```JavaScript
var str = "Hello World!";
var res = str.toLowerCase();  //hello world!
```

######7. toUpperCase() converts a string to uppercase letters
```JavaScript
var str = "Hello World!";
var res = str.toUpperCase();  //HELLO WORLD!
```

######8. substring() returns a subset of a string between one index and another, or through the end of the string
```JavaScript
var str = "Hello world!";
var res = str.substring(1, 4);  //ell - index 1, 2 and 3
```

######9. substr() extracts parts of a string, beginning at the character at the specified position, and returns the specified number of characters
```JavaScript
var str = "Hello world!";
var res = str.substr(1, 4);  //ello - index 1, 2, 3 and 4
```

######10. splice() changes the content of an array by removing existing elements and/or adding new elements
```JavaScript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi");  //Banana,Orange,Lemon,Kiwi,Apple,Mango
```

######11. indexOf() returns the position of the first occurrence of a specified value in a string
```JavaScript
var str = "Hello world, welcome to the universe.";
var n = str.indexOf("e");  //1
```

######12 .filter() creates a new array with all elements that pass the test implemented by the provided function
```JavaScript
function isBigEnough(value) {
  return value >= 10;
}
var filtered = [12, 5, 8, 130, 44].filter(isBigEnough);  //filtered is [12, 130, 44]
```

######13. sort() sorts the elements of an array in place and returns the array
```JavaScript
var fruit = ['cherries', 'apples', 'bananas'];
fruit.sort();  // ['apples', 'bananas', 'cherries']

var points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a-b}); //[1,5,10,25,40,100]
```

######14. charAt() returns the character at the specified index in a string
```JavaScript
var str = "HELLO WORLD";
var res = str.charAt(0); //H
```

######15. fromCharCode() converts a Unicode number into a character
```JavaScript
var res = String.fromCharCode(65); //A
```

######16. charCodeAt() returns the Unicode of the character at the specified index in a string
```JavaScript
var str = "HELLO WORLD";
var n = str.charCodeAt(0); //72
```

######17. parseInt() Parses a string and returns an integer
```JavaScript
var a = parseInt("10")  //10
```

######18. Math.round() Round a number to the nearest integer
```JavaScript
Math.round(2.5);  //3
```

######19. Math.floor() Round a number downward to its nearest integer
```JavaScript
Math.floor(1.6);  //1
```

######20. Math.max() Returns the largest of zero or more numbers
```JavaScript
Math.max(10, 20);  //20
```

######21. Math.min() returns the smallest of zero or more numbers
```JavaScript
Math.min(10, 20);  //10
```

######22. reduce() applies a function against an accumulator and each value of the array to reduce it to a single value
```JavaScript
var total = [0, 1, 2, 3].reduce(function(a, b) {
  return a + b;
}, 0);  //total == 6
```
