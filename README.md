# Coding Standards

## HTML

## LESS // CSS

## Javascript Guidelines

### General
 
* Use [JSDoc](http://usejsdoc.org/about-getting-started.html) syntax to document code.

### Naming conventions

* Functions : camelCase
* Variables : camelCase
* Class Names : CapsOnEachWord
* Constants : ALL_CAPS

### Style conventions

* Always use semicolons.
* Avoid polluting the global scope. Wrap code in [iifies](http://benalman.com/news/2010/11/immediately-invoked-function-expression/).

```javascript
(function($){
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
* http://javascript.crockford.com/code.html
* http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml
* http://contribute.jquery.org/style-guide/js/
