# Module 2 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

*Note: any topics from the first assessment should be reviewed in addition to the questions below!*

## CSS

### Questions

1. What is the box model?
- It is a way to describe the borders and spacing in between the boxes of each tag.

2. What is the difference between block and inline elements?
- A block element will span the full width of a container.  An inline element don't try to take more width than they need.

3. What is responsive design?
- Responsive design makes your webpage look good on all devices.  It is about using CSS and HTML to resize, shrink, enlarge, or moves the content to make it look good on any screen.

4. Which selector is more specific, a tag selector or class selector?
- Class selector is more specific, it is a way to add a specific style to one tag, but not the other.

5. What does `box-sizing` do?
- If we want width and height of a box to stay the same when we add padding and borders to a box, there is a box-sizing value called border-box that helps us achieve this. i.e. box-sizing: border-box; 

6. What's the difference between `relative` and `absolute` positioning?
-Relatively positioned elements stack one on top of the next, these elements are in the normal flow.  You can shift these elements around using offset properties such as: top, right, bottom, and left.  
-Absolutely positioned elements are removed from the normal flow, they can be positioned anywhere, they will not affect or be affected by any other element in the flow.  Absolutely positioned elements also use offset properties.

### Exercises

1. Write a CSS rule to turn the background color of the link with the `.btn` class blue on hover:

  ```html
  <a href="#" class="btn">Learn more</a>
  ```
.btn a:hover{
    background-color: blue;
 }
2. Write a CSS rule to give the `.container` a maximum width of `980px` when the browser window is wider than `1200px`:

  ```html
  <div class="container">
    <h1>I'm a heading!</h1>
  </div>
  ```
  
  - .container{
    margin: 0 auto;
    max-width:980px;
    }

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
- Third paragraph.

4. Open this [JSBin](http://jsbin.com/qigiwuhepe/1/edit?html,css,output). Write a CSS rule using floats to make the HTML sample into a four column layout. Paste your udpated link below.
-http://jsbin.com/debuciruno/1/edit?html,css,output
-.column{
  float:left;
  }

.column.fourth{
  width:25%
}

## JavaScript

### Questions

1. What is a callback?
- Callback is a function passed to another function as a parameter.  It gets called or executed in the other function.

### Exercises

1. Write a function `filterLongWords()` that takes an array of words and an integer `num` and returns the array of words that are longer than `num`.
-var filterLongWords = function(arrWords, num){
  var a=[];
  for(var i=0; i<arrWords.length; i++){
    if(arrWords[i].length > num){
      a.push(arrWords[i]);
    }
  }
  console.log([a]);
}
filterLongWords(["Happy","kind","lovely"], 4);

http://jsbin.com/woliyujotu/1/edit?html,js,console

2. Write a function `charFreq()` that takes a string and builds a frequency listing of the characters contained in it. Represent the frequency listing as a Javascript object. Try it with something like `charFreq("abbabcbdbabdbdbabababcbcbab")`.
-function charFreq (string){
  var list = {};
  var length = string.length;
  for (var i = 0; i<length; i++){
    if (string.charAt(i) in list)
    list[string.charAt(i)] += 1;
    else
    list[string.charAt(i)] = 1;
  }
  console.log(list);
}
charFreq("abbabcbdbabdbdbabababcbcbab");
http://jsbin.com/duhuzosodu/1/edit?html,js,console

## DOM Scripting

### Questions

1. What does DOM stand for and what is it?
-DOM stands for Document object model.  When a browser loads a page it uses DOM to interpret each of the document's element as an object(node). The DOM builds a tree of objects that is accessible to Javascript.

### Exercises

1. Write a JavaScript statement that finds the element with the ID, `next`, and saves it to a variable called `nextButton`:

  ```html
  <a href="#" id="next" class="btn">Next</a>
  ```
  - var nextButton = document.getElementById('next');

2. Write another line that updates the text of `nextButton` to `"Next image"`.
- nextButton.textContent="Next image";

3. Write another line that adds a click event listener to `nextButton` so that when it's clicked the browser alerts `"Next image coming up."`.
-nextButton.addEventListener("click", function(event){
      alert("Next image coming up.");
      });

## jQuery

### Questions

1. What is a JavaScript library and why do we use them? 
-A Javascript library is a library of pre-written Javascript which allows for easier development of javascript based applications. These libraries execute many common, timing-consuming tasks.

2. What is jQuery for?
-jQuery is a well-written javascript code.  It is a fast and concise javascript library that simplifies HTML document traversing, event handling, animating for rapid web development. It has no cross-browser compatibility issues.

### Exercises

1. Write a statement to select all elements with the `.btn` class using a jQuery selector and save them to a variable called `buttons`:

  ```html
  <a href="#" id="next" class="btn">Next</a>
  <a href="#" id="beginning" class="btn">Beginning</a>
  <a href="#" id="previous" class="btn">Previous</a>
  ```
  - var $buttons=$('.btn');
   $buttons.find('.btn');

2. Write another line that adds a click event to the buttons that logs `'click'` to the console when the button is clicked. Use the jQuery syntax.
-$(buttons).click(clickHandler);

var clickHandler = function(){
console.log("click");
};

## Angular

### Questions

1. How is a framework different than a library?
-A framework, like Angular, provides the basic structure of an application. The "framework" is in charge and our code fills in the details.  A library, such as jQuery, is a collection of pre-written code consisting of common tasks that simplify development. Our code is in charge and uses a library to retrieve specific functions from the collection.

2. What is a controller?
- Controllers contain the business logic that apply functions and values to the scope. They do not share code between each other.

3. What is a view?
-Model is the data of an application.  The view is the output representation of that data or the UI(user interface).

4. What is a single page application?
-Single page applications are web apps that load a single HTML page and dynamically update that page as the user interacts with the app.

5. What is a directive in Angular?
-An Angular element in HTML is a directive.  It binds angular functionality to HTML on a page.

## Git

### Exercises

1. Write a command to create a new branch called `bug-fix`.
git branch bug-fix

2. If you're on the `master` branch, write a command to merge a branch called `bug-fix` into the `master` branch.
git merge bug-fix
