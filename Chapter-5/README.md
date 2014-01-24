# SASS Style Guide

#### As SASS is nothing but an extension of CSS, all the rules that apply to CSS apply to SASS.

1. You should not nest selectors more than 4 levels deep. There are legitimate use cases for why you might want to do this, but be prepared to support your decision. 
2. At the moment, and for the foreseeable future, we are using [Bootstrap](http://getbootstrap.com/). In order to ensure that we utilize it to its full potential, we should use Bootstrap's existing `@mixin`'s and helper classes. If you find that the existing infrastructure is lacking in someway, feel free to extend the existing classes and `@mixin`s.

SASS can get out of control rather quickly. In order to ensure that the code is always readable, there are a few organization patterns we will use.

### Ordering selectors

Selectors should be nested in the following heirarchy, the idea being that selectors go from __least specific__ to __most specific__.

 1. HTML tags: `<table>`, `<p>`, `<form>`, etc.
 2. Classes: `.voyager`, `.deep-space-nine`, `.enterprise`, etc., [excluding references to parent selectors](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#referencing_parent_selectors_).
 3. References to parent selectors are at the bottom, whether they are a psuedo selector (`:hover`), or a chained class (`.rio-grande`)
 4. The heiarchy resets within each nest selector

```sass
.enterprise {
    table {
        // stuff
    }
    
    .picard {
        // Tea. Earl Grey. Hot
        td {
            // more
        }
        
        .worf {
            // This code has honor
        }
    }
    
    &:last-child {
        // even more
    }
}

```

<table><tr><td><a href="../Chapter-4/README.md">&larr; Previous</a></td><td><a href="../Chapter-6/README.md">Next &rarr;</a></td></tr></table>
