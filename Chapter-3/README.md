# JavaScript Style Guide

#### For anything not covered here, please refer to the [Google JavaScript Styleguide](http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml)

1. Use 4 space indentation per tab.
2. There should be exactly one space before and after the parenthesis in a function declaration or conditional.
3. Always start your curley braces on the same line as the thing they opening.
4. Break up object literals into multiple lines for readability.
5. Any function that returns a boolean or is truthy should be named in such a way that it is immediatly apparent. For example, `is`, `has`, `should`, etc.
6. Define variables at the top of the scope they are going to be used in.
7. [Camel case](http://en.wikipedia.org/wiki/CamelCase) all your variables and things.
8. __Don't__ rely on implicit semi-colon insertion. Do it yourself. For a good read on why relying on implcit semi-colon insertion is bad practice, [read this](http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml?showone=Semicolons#Semicolons).
9. Strings should be in single quotes.

### Wrong way to write JavaScript

```javascript
if(foo){
  console.log("It's a bit cramped here");
}

function property_check(object, property){
    if(object.hasOwnProperty(property)){
        return true;
    }
    return false;
}
```

### Right way to write JavaScript

```javascript
if (foo) {
    console.log('Science is fun');
}

function portals() {
    return 'The cake is a lie';
}

function hasProperty(object, property) {
    if (object.hasOwnProperty(property)) {
        return true;
    }
    return false;
}
```

<table><tr><td><a href="../Chapter-2/README.md">&larr; Previous</a></td><td><a href="../Chapter-3/README.md">Next &rarr;</a></td></tr></table>
