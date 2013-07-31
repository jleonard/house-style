# Coding Standards

## HTML

### General

* 2 space indentation, no tabs
* lowercase only
* Use elements (sometimes incorrectly called “tags”) for what they have been created for. 
e.g. use heading elements for headings, p elements for paragraphs, a elements for anchors, etc.
* Separate structure from presentation from behavior i.e. no inline styles, no inline javascript
* use double quotes around attributes, not single quotes. e.g. src="images/my-image.png"
* use IDs sparingly and correctly.  IDs may be used for specific elements that need to be targeted.  They may be used for
their hash property in the browser (like an anchor link).
* use classes sparingly and correctly.  Classes are meant to be re-used, so if you find yourself 
duplicating styles for two different classes, consider consolidating the style into one class.


## LESS // CSS

### General

* 2 space indentation, no tabs
* lowercase only
* do not use element names in conjunction with class names
e.g. .error{...} NOT div.error{...}
* use only dashes to separate multi-word class/div names e.g. #my-div, .my-class
* use single quotes around attributes e.g. background: url('images/bg.png')
* separate sections using a section comment 
/*navigation*/
.nav-button{
}

## Javascript Guidelines

### General
 
* Use [JSDoc](http://usejsdoc.org/about-getting-started.html) syntax to document code.

### Naming conventions

* Functions : camelCase
* Variables : camelCase
* Class Names : CapsOnEachWord
* Constants : ALL_CAPS_WITH_UNDERSCORES

### Style conventions

* Always use semicolons.
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

#### Further Reading
* http://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml
* http://javascript.crockford.com/code.html
* http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml
* http://contribute.jquery.org/style-guide/js/
