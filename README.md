# Coding Standards

## HTML

### General

* Lowercase only.
* 2 space indentation, no tabs.
* Use elements for what they have been created for. 
e.g. use heading elements for headings, p elements for paragraphs, a elements for anchors, etc.
```HTML
 <!--Avoid-->
 <div class="anchor"></div>

 <!--Do-->
 <a href="http://www.google.com"></a>
```
* Separate structure from presentation and from behavior.
```HTML
 <!--Avoid-->
 <button style="margin-top: 10px;" onclick="onClickHandler"></button>

 <!--Do -->
 <button class="exit-button"></button>
 <script>
  $('.exit-button').on('click', function(){
    //handle interactions with javascript only
   });
 </script>
```
* Use double quotes around attributes, not single quotes.
```HTML
 <!--Avoid-->
 <img src='images/my-image.png' />

 <!--Do-->
 <img src="images/my-image.png" />
```
* Use IDs sparingly and correctly.  IDs may be used for specific elements that need to be targeted.  They may be used for
their hash property in the browser (like an anchor link).
* Use classes sparingly and correctly.  Classes are meant to be re-used, so if you find yourself 
duplicating styles for two different classes, consider consolidating the style into one class.

## LESS // CSS

### Naming conventions
* Do not use element names in conjunction with class names.
```Less
 // Avoid
 div.error{
  ... 
 }

 //Do - use stylename only
 .error{
  ...
 }
```
* Use only dashes to separate multi-word class and div names.
```Less
 // Avoid
 #myDiv{
  ...
 }
 #my_div{
  ...
 }
 
 // Do - use dashes and all lowercase
 #my-div{
  ...
 }
```


### Style conventions

* 2 space indentation, no tabs.
* Lowercase only.
* Use single quotes around attributes.
```Less
 // Avoid
 background: url("images/bg.png")
 
 // Do - use single quotes
 background: url('images/bg.png');
```
* Separate sections using a section comment.
```Less
 /*navigation*/
 .nav-button{
  ...
 }
```

## Javascript Guidelines

### General
 
* Use [JSDoc](http://usejsdoc.org/about-getting-started.html) syntax to document code.

### Naming conventions

* Functions : camelCase
* Variables : camelCase
* Class Names : CapsOnEachWord
* Constants : ALL_CAPS_WITH_UNDERSCORES
* Filenames : all-lower-case-with-dashes.js
* Accessor functions should be named as follows:
```javascript
 
 //getter
 getMyVar : function(){
 };
 
 //setter
 setMyVar : function(value){
 }
 
 //boolean
 isMyVar : function(){
 };
```


### Style conventions

* Always use semicolons.
* Keep strings in single quotes so that html may easily be written into strings.
```javascript
 var htmlBlock = '<div class="my-class"></div>';
```

* Avoid polluting the global scope. Wrap code in [iifies](http://benalman.com/news/2010/11/immediately-invoked-function-expression/).
```javascript
(function($){
  "use strict";
  // Hello, I'm an iife (Immediately Invoked Function Expression)
})(jQuery);
```
* Variables should be declared before used. Each variable should have it's own line and comment.
```javascript 
    // Avoid
    var currentEntry, level, size;
    
    // Do - Make your variables easy to read and add space for line comments.
    var currentEntry; // currently selected table entry
    var level;        // indentation level
    var size;         // size of table
```
* Do not use multi-line string literals.
```javascript
   // Avoid
   var myString = 'A rather long string of English text, an error message \
                actually that just keeps going and going -- an error \
                message to make the Energizer bunny blush (right through \
                those Schwarzenegger shades)! Where was I? Oh yes, \
                you\'ve got an error and all the extraneous whitespace is \
                just gravy.  Have a nice day.';
                
   // Do - concatenate lines; even better: use templates!
   var myString = 'A rather long string of English text, an error message ' +
    'actually that just keeps going and going -- an error ' +
    'message to make the Energizer bunny blush (right through ' +
    'those Schwarzenegger shades)! Where was I? Oh yes, ' +
    'you\'ve got an error and all the extraneous whitespace is ' +
    'just gravy.  Have a nice day.';
```
* Keep open braces on the line they are opening.
```javascript
 // Avoid
 var obj = { "key" : "value" };
 var arr = [0, 1, 2, 3];
 function test(){ ... }
 function test()
 {
  ...
 }
 
 // DO
 var obj = {
  "key" : "value"
 }
 
 var arr = [
  0,
  1,
 ]

 function test() {
  ...
 }
```


#### Further Reading
* http://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml
* http://javascript.crockford.com/code.html
* http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml
* http://contribute.jquery.org/style-guide/js/
