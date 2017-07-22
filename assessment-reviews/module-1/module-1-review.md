# Module 1 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

## HTML

### Questions

1. What is HTML and what is it used for?
- HTML is Hypertext Markup Language.  It is used to create online documents called webpages.

2. What is the difference between an ID and a class?
-A class selector is most often used on several elements to set a particular style for many HTML elements, while ID is unique to only one element.

3. What does it mean to write "semantic" HTML?
-Semantic HTML introduces meaning to the webpage rather than just presentation. eg. <p>.  Semanantic tags provide information about the contents of the tags that goes beyond just how they look on a page.

### Exercises

1. Write a paragraph tag with a class of "highlight" and content "Watch out!".
- <p class ="highlight"> "Watch Out!" </p>

2. Write an HTML image tag to show an image called `profile-picture.jpg`.
<img = src="profile-picture.jpg">

3. Write a link tag that links to http://google.com.
<link href="http://google.com">

5. Write an complete standard HTML document outline (including a DOCTYPE, and `<html>`, `<head>`, and `<body>` tags).
<html>
  <head>
    <link>
   </head>
   <body>
   ....
   </body>
  </head>
 </html>
    
6. Inside of the code for the previous exercise, write the appropriate tag to link to a script file called `main.js`.
<html>
  <head>
    <script src="main.js"></script>
   </head>
   <body>
   ....
   </body>
  </head>
 </html>

7. Inside of the code for the previous exercise, write the appropriate tag to link to a stylesheet file called `main.css`.
<html>
  <head>
    <link type="text/main.css">
   </head>
   <body>
   ....
   </body>
  </head>
 </html>

8. Write a numbered list in HTML and list three of your favorite books.
<ol>
<li>"Is Everyone Hanging out Without me" - by Mindy Kaling</li>
<li>"The Story of My Life" - by Helen Keller</li>
<li>"Three cups of Tea: One man's mission to promote peace... One school at a time" - by Greg Mortenson</li>
</ol>
    
  
9. Fix the indentation of the following HTML sample:

  <html>
    <div>
      <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
     </ul>
   </div>
 </html>
 

## CSS

### Questions

1. What is CSS and what is it used for?
-Cascading style sheet. It is a language used to describe the presentation of webpages including color, layouts, and font.

2. What is the CSS box model?
- CSS box model references the design and layout of the HTML elements. It refers to how properties such as margins, padding, borders, and content of each element are calculated in conjunction with another.

3. What's the difference between margin and padding?
- Margin is the area around the border while padding is area around the content.

### Exercises

1. Write a CSS rule to make the text of all `h1` tags red.
- h1{
      color: red;
     }
2. Write a CSS rule to make the background color of the link with `class="btn"` blue:
 .btn{
 background-color: blue;
 }
 
  ```html
  <a href="#" class="btn">Learn more</a>
  ```

3. Write a CSS rule to give the first paragraph in the following HTML a font size of `20px`, but not the second paragraph.
.jumbotron p{
  font-size: 20px;
  }

  ```html
  <header class="jumbotron">
    <p>Hello, World!</p>
  </header>

  <p>Welcome to this awesome website!</p>
  ```

## JavaScript

### Questions

1. What is a function? What are they used for? 
- A function "does something" step-by-step that we need to do repeatedly.

2. What is the difference between `==` and `===`?
-Both values on either side of == should be the same.  Both value and type on either side of === should be the same.
Say x=5, then x==5 is true while x==='5' is false.

3. What is the difference between global and local scope variables?
-Within function scope of variable is local i.e. variable can be accessed only locally.  variables declared outside the function are glocal i.e. they are accessible from anywhere.

4. What is a boolean value?
- A boolean value is true or false.

5. What is an array?
-An array is a data structure with automatically indexed positions.

### Exercises

1. Write a line that declares a variable called `myName` and set its value to your name.
- var myName = "Siscely George";

2. Write a loop that logs the numbers 1 through 10 to the console.
for (i=1; i<=10; i++){
console.log(i);
}

3. Translate the following pseudocode into JavaScript: if `score` is greater than `3` and `lives` is greater than `0`, alert "You win!".
- if (score>3 && lives>0){
      alert("You Win!");
      }
4. Write a function `sayHello` that takes one argument, a name, and logs "Hello, <name>!" to the console. Then, call the function below the function definition and pass in your name as the argument.
- function sayHello(name){
console.log("Hello" + name);
}
sayHello(Siscely);

5. What would the following script log to the console?
"Friday, Friday"

  ```javascript
  var currentSong = "Call Me Maybe";

  function setSong(song) {
    currentSong = song;
  }

  setSong("Friday, Friday");

  console.log(currentSong);
  ```

6. What would the following script log to the console?
- 10

  ```javascript
  var add = function(a, b) {
    return a + b;
  }

  var result = add(3, 7);

  console.log(result);
  ```

7. What would the following script log to the console?
- Hello Sarah ! Goodbye Sarah !

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

8. Write a function `findLongestWord()` that takes an array of words and returns the length of the longest one.
var words = ["Hello Sarah", "Goodbye Sarah", "console", "array", "function"];
var lgth=0;
var findLongestWord = function(words){
for (var i = 0; i < words.length; i++){
if (words[i].length > lgth){
 var lgth = words[i].length;
 longest = words[i];
  }
 }
 return longest;
 }

9. Define a function `sum()` that sums all the numbers in an array of numbers. For example, `sum([1,2,3,4])` should return 10.
var num = [1, 2, 3, 4];
var total = 0;
var sum = function(num){
for (var i =0; i < num.length; i++){
var total = sum[i] + total;
}
return total;
}

10. Write a function that takes a character (i.e. a string of length 1) and returns true if it is a vowel, false otherwise.

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

12. Using the same script as above, write the correct line to log the dog's name to the console.

## Command Line

### Questions

1. What is the command line and what is it used for?
2. What does the command `ls` do?
3. What does the command `pwd` do?
4. What does the following command do: `cd my-cool-project`

### Exercises

1. Write the command to make a new directory called "my-cool-project".
2. Write the command to create a file called "index.html".
3. Write the command to delete a file called "main.css".

## Git

### Questions

1. What is Git and what is it used for?
2. What's the difference between a local repository and a remote repository?

### Exercises

1. Write the command that you would use to create a new local Git repository.
2. Write the command to stage a file called `index.html` to be committed.
3. Write the command to view the current status of the git repository.
