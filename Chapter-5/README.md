# SASS Style Guide

#### As SASS is nothing but an extension of CSS, all the rules that apply to CSS apply to SASS.

1. You should not nest selectors more than 4 levels deep. There are legitimate use cases for why you might want to do this, but be prepared to support your decision. 
2. At the moment, and for the foreseeable future, we are using [Bootstrap](http://getbootstrap.com/). In order to ensure that we utilize it to its full potential, we should use Bootstrap's existing `@mixin`'s and helper classes. If you find that the existing infrastructure is lacking in someway, feel free to extend the existing classes and `@mixin`s.

### Wrong way to write SASS

```Sass
.foo {
    position: absolute;
    .bar {
        border: 1px solid #CCC;
        &:hover {
            background: #232323;
            .cat {
                -webkit-filter: blur(.2em)
            }
        }
    }
}
```

### Right way to write SASS

```Sass
.foo {
    position: absolute;
    
    .bar {
        border: 1px solid #CCC;
    }

    &:hover {
        background: #232323;
    }
    
    .cat {
        -webkit-filter: blur(.2em);
    }
}
```

##### As a note, the above code is not tested. The point is that selectors nested more than 3 levels deep can be difficult to follow. Try and refactor, if possible, so that you can reduce nesting.

<table><tr><td><a href="../Chapter-4/README.md">&larr; Previous</a></td><td><a href="../Chapter-6/README.md">Next &rarr;</a></td></tr></table>
