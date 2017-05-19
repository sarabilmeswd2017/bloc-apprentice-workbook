# Module 1 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

## HTML

### Questions

1. What is HTML and what is it used for? Hyper Text Markup Language, to create web pages
2. What is the difference between an ID and a class? classes can be used many times on a page, IDs can only be used once. You call a class by .classname, and you call an ID by #IDname
3. What does it mean to write "semantic" HTML? it means that the html gives meaning to the web page, for example a <p> tag means it is a paragraph

### Exercises

1. Write a paragraph tag with a class of "highlight" and content "Watch out!".
```<p class="highlight"> Watch out!</p>```
2. Write an HTML image tag to show an image called `profile-picture.jpg`. 
```<img src="profile-picture.jpg">```
3. Write a link tag that links to http://google.com. 
```<a href="http://google.com">Google</a>```
5. Write an complete standard HTML document outline (including a DOCTYPE, and `<html>`, `<head>`, and `<body>` tags).
```<!DOCTYPE html>
<html>
<head>
<script src="main.js"></script>
<link rel="stylesheet" href="main.css">
</head>
<body>
<ol>
 <li>Harry Potter</li>
 <li>Pride and Prejudice</li>
 <li>The Five People You Meet in Heaven</li>
</ol>

</body>
</html>```
6. Inside of the code for the previous exercise, write the appropriate tag to link to a script file called `main.js`.
7. Inside of the code for the previous exercise, write the appropriate tag to link to a stylesheet file called `main.css`.
8. Write a numbered list in HTML and list three of your favorite books.
9. Fix the indentation of the following HTML sample:

  ```html
  <div>
   <ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
   </ul>
  </div>
  ```

## CSS

### Questions

1. What is CSS and what is it used for? 
It means Cascading Style Sheets. It is used to give your web page (your html), style. 
2. What is the CSS box model? 
The box model is a box that wraps aroudn every element. The box has content, around the content is padding, around the padding is a border, and around the border is a margin. 
3. What's the difference between margin and padding? 
padding is right outsite the content. margin is outside the border. 

### Exercises

1. Write a CSS rule to make the text of all `h1` tags red. 
```h1 {color: red; } ```
2. Write a CSS rule to make the background color of the link with `class="btn"` blue: 
```.btn {background-color:blue;}```

  ```html
  <a href="#" class="btn">Learn more</a>
  ```

3. Write a CSS rule to give the first paragraph in the following HTML a font size of `20px`, but not the second paragraph.
```.jumbotron{font-size:20px;}```

  ```html
  <header class="jumbotron">
    <p>Hello, World!</p>
  </header>

  <p>Welcome to this awesome website!</p>
  ```

## JavaScript

### Questions

1. What is a function? What are they used for? 
A function is something that we give input, and it gives us output. It is used when we want to do the same actions repeatedly. 
2. What is the difference between `==` and `===`? 
== means equal to, but it wont recognize the type, so 4 and "4" would look the same to ==, but === recognizes the type, and would realize that "4" is a string.
3. What is the difference between global and local scope variables?
A global variable is declared outside of a functino and can be accessed by any function. A local variable is declared inside a function and can only be accessed by that function. 
4. What is a boolean value? 
true or false
5. What is an array?
It is a special variable that can hold more than one value at a time (and diff types), the values are automatically indexed. We used [ ] to write arrays. 

### Exercises

1. Write a line that declares a variable called `myName` and set its value to your name.
var myName = "Sara Yocheved Bilmes";
2. Write a loop that logs the numbers 1 through 10 to the console.
var x =1;
for(var x =1;x <= 10;x++){
  console.log(x);
}
3. Translate the following pseudocode into JavaScript: if `score` is greater than `3` and `lives` is greater than `0`, alert "You win!".
if((score > 3) && (lives > 0)){
   alert("You win!");
   }
4. Write a function `sayHello` that takes one argument, a name, and logs "Hello, <name>!" to the console. Then, call the function below the function definition and pass in your name as the argument.

var sayHello = function(name){
  return "Hello, " + name + "!";
};
console.log(sayHello("Sara Bilmes"));
5. What would the following script log to the console?

  ```javascript
  var currentSong = "Call Me Maybe";

  function setSong(song) {
    currentSong = song;
  }

  setSong("Friday, Friday");

  console.log(currentSong);
  ```
  "Friday, Friday"

6. What would the following script log to the console?

  ```javascript
  var add = function(a, b) {
    return a + b;
  }

  var result = add(3, 7);

  console.log(result);
  ```
  10

7. What would the following script log to the console?

  ```javascript
  var helloGoodbye = function(name) {
    return sayHello(name) + " " + sayGoodbye(name);
  }

  var sayHello = function(name) {
    return "Hello " + name " !";
  }

  var sayGoodbye = function(name) {
    return "Goodbye " + name " !";
  }

  console.log(helloGoodbye("Sarah"));
  ```
An error...there are no second + in sayHello and say Goodbye

8. Write a function `findLongestWord()` that takes an array of words and returns the length of the longest one.

``` var array = ["apple", "peach", "Star fruit"];
function findLongestWord(){
 var length = 0;
  for(var i = 0;i < array.length;i++) {
    if(array[i].length > length){
       length = array[i].length;
       }
     }
  return length;
}
console.log(findLongestWord(array));```
9. Define a function `sum()` that sums all the numbers in an array of numbers. For example, `sum([1,2,3,4])` should return 10.
/* Define a function `sum()` that sums all the numbers in an array
of numbers. For example, `sum([1,2,3,4])` should return 10. */

function sum(numbers) {
  // loop through the array of numbers
  // create a variable to store the current total (set to 0)
  // add the current number to the current total
  // return the total
  var curTotal = 0;
  for(var i = 0;i < numbers.length;i++){
    curTotal = numbers[i] + curTotal;
  }
  console.log(curTotal);
  return curTotal;
}

sum([1, 2, 3, 4, 5, 6, 7, 8]);

// Define the function and determine the inputs
// Define the inputs as arguments
// Write pseudocode to sketch the steps for how the function might work
// Translate each line into javascript and test as you go with console logs
// Adjust the logic if it doesn't work, and repeat!
10. Write a function that takes a character (i.e. a string of length 1) and returns true if it is a vowel, false otherwise.

```function isVowel(x){

  if(x == "A" || x == "a" || x == "E" || x == "e" || x == "I" || x == "i" || x == "O" || x == "o" || x == "U" || x== "u") {
            return true;
        }
        else{
            return false;
        }
     }
console.log(isVowel("o"));```
11. Write the correct line to make `"Woof!"` show up in the console based on this script:

  ```javascript
  var pet = {
    name: "Charles",
    goodDog: true,
    speak: function() {
      console.log("Woof!");
    }
  };
  ```
  pet.speak();

12. Using the same script as above, write the correct line to log the dog's name to the console.
console.log(pet.name);

## Command Line

### Questions

1. What is the command line and what is it used for?
A text interface for your computer. you can use it to navigate around your computer, add files, delete files..ect..
2. What does the command `ls` do?
looks at the directory you are in and tells you all the files and folders in that directory
3. What does the command `pwd` do? 
outputs the directory you are in
4. What does the following command do: `cd my-cool-project`
changes directory to my-cool-project

### Exercises

1. Write the command to make a new directory called "my-cool-project".
mkdir my-cool-project
2. Write the command to create a file called "index.html".
touch index.html
3. Write the command to delete a file called "main.css".
rm main.css

## Git

### Questions

1. What is Git and what is it used for? 
Git is a Version Control System that is used for tracking files on computer systems and coordinates work on those files among multiple people. It is used when a lot of people are working on a project. 
2. What's the difference between a local repository and a remote repository?
local repository is on your computer, and a remote respository is in computer heaven. Everyone can have acces to the remote repository. 

### Exercises

1. Write the command that you would use to create a new local Git repository.
git init
2. Write the command to stage a file called `index.html` to be committed.
git add index.html
3. Write the command to view the current status of the git repository.
git status
