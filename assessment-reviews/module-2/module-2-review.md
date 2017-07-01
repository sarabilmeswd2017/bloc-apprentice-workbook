# Module 2 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

*Note: any topics from the first assessment should be reviewed in addition to the questions below!*

## CSS

### Questions

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

*Note: any topics from the first assessment should be reviewed in addition to the questions below!*

## CSS

### Questions

1. What is the box model? 
Its a box that wraps around every element in html. first there is the content, then the padding, then the border, then the margin
2. What is the difference between block and inline elements?
inline elements display horizontal, block elemnts display vertical. Block elemtns take up a new line and fill the width.
3. What is responsive design?
when the design is suitable for mobile and tablet devices. the layout switches around to work with the device
4. Which selector is more specific, a tag selector or class selector? 
class selector
5. What does `box-sizing` do?
it makes it so that you include the whole box (if you do box-sizing:border-box) , in the width, so you dont have issues with width
6. What's the difference between `relative` and `absolute` positioning?
absolute posititong takes the object totally out of the site, it can go absoltely anywhere relative to the screen. relative positioning places an object relative to its normal position. but an absolutely positioned element will be relative to its parent if its parent is positioned relative

### Exercises

1. Write a CSS rule to turn the background color of the link with the `.btn` class blue on hover:

  ```html
  <a href="#" class="btn">Learn more</a>
  ```
  ```.btn:hover{
      background-color:blue;
  }```

2. Write a CSS rule to give the `.container` a maximum width of `980px` when the browser window is wider than `1200px`:

  ```html
  <div class="container">
    <h1>I'm a heading!</h1>
  </div>
  ```
  
```  @media (min-width: 1200px) {
     .container{max-width:980px;
     }```

3. Which text would be red in the following example?

  ```html
  <style>
    section p:last-child {
      color: red;
    }
  </style>

  <section>
    <p>First paragraph</p>
    <p>Second paragraph</p>
    <p>Third paragraph</p>
  </section>
  <section>
    <p>First paragraph</p>
    <p>Second paragraph</p>
    <p>Third paragraph</p>
  </section>
  ```
Third Child
4. Open this [JSBin](http://jsbin.com/qigiwuhepe/1/edit?html,css,output). Write a CSS rule using floats to make the HTML sample into a four column layout. Paste your udpated link below.

http://jsbin.com/xekarinuli/edit?html,css,output
## JavaScript

### Questions

1. What is a callback?
its a function passed to another function

### Exercises

1. Write a function `filterLongWords()` that takes an array of words and an integer `num` and returns the array of words that are longer than `num`.

```
function filterLongWords(array, num) {
  var newArray = [];
  for(var i =0;i < array.length;i++){
    if(array[i].length > num){
      newArray.push (array[i]) ;
    }
  }
  return newArray;
}
```

2. Write a function `charFreq()` that takes a string and builds a frequency listing of the characters contained in it. Represent the frequency listing as a Javascript object. Try it with something like `charFreq("abbabcbdbabdbdbabababcbcbab")`.

```
function charFreq(string){
  
    var frequencyCount = {};
    
    for(var i =0; i < string.length;i++){
      var currentLetter = string.charAt(i);
      if(frequencyCount[currentLetter]){
        frequencyCount[currentLetter]++;
      }else{
        frequencyCount[currentLetter] = 1;
      }
     
    }
    return frequencyCount;
  }
  ```

## DOM Scripting

### Questions

1. What does DOM stand for and what is it?
Document Object Model. Its how we integrate javascript into html

### Exercises

1. Write a JavaScript statement that finds the element with the ID, `next`, and saves it to a variable called `nextButton`:

  ```html
  <a href="#" id="next" class="btn">Next</a>
  ```
`var nextButton = document.getElementById("next");`
2. Write another line that updates the text of `nextButton` to `"Next image"`.
`nextButton.innerHTML = "Next image"`
3. Write another line that adds a click event listener to `nextButton` so that when it's clicked the browser alerts `"Next image coming up."`.
nextButton.addEventListener('click', function(){
alert("Next image coming up");
})

## jQuery

### Questions

1. What is a JavaScript library and why do we use them?
Its a library of pre-written javascript, allows for easier development
2. What is jQuery for?
Its simpler, it loads pages faster, it works on all browsers, easy to learn...
### Exercises

1. Write a statement to select all elements with the `.btn` class using a jQuery selector and save them to a variable called `buttons`:

  ```html
  <a href="#" id="next" class="btn">Next</a>
  <a href="#" id="beginning" class="btn">Beginning</a>
  <a href="#" id="previous" class="btn">Previous</a>
  ```
```
var buttons = $(".btn");

```
2. Write another line that adds a click event to the buttons that logs `'click'` to the console when the button is clicked. Use the jQuery syntax.

THS DOES NOT WORK...

```
$("buttons").click(function(){
   console.log("click");
}
```


## Angular

### Questions

1. How is a framework different than a library?
A Library is a reusable piece of code which you use as it comes, no hooks to extend to. A framework is a piece of code which dictates the architecture of your project. There are hooks and callbacsk,..you build on it. 
2. What is a controller?
it controlls the data. you use ng-controller to call it
3. What is a view?
the html. what you see
4. What is a single page application?
they load a single html page and dynamically update hte page as the user interacts with the app
5. What is a directive in Angular?
ways to extend your html. examples include ng-app, ng-init, ng-model

## Git

### Exercises

1. Write a command to create a new branch called `bug-fix`.
git checkout -b bug-fix
2. If you're on the `master` branch, write a command to merge a branch called `bug-fix` into the `master` branch.
git merge bug-fix
