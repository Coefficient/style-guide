# CSS Style Guide

1. Hyphenate your class names.
2. Write modular, reusable CSS.
3. Don't overqualify selectors.
4. Use 4 spaces per tab.
5. Place the opening brace on the same line as the selector
6. Try to order properties according to their purpose. The tendancy has been to order properties related to layout on the top and properties related to visuals at the bottom.
7. Use `em` as your unit of measurement where it makes sense. Use percentages in other places. Avoid pixels.

### Wrong way to write CSS

```CSS
div.foo
{
    float: left;
    color: whitesmoke;
    width: 33%;
    border: 1px solid #CCC;
}
```

```HTML
<div class="foo">
    <p>It's nice in here.</p>
</div>
```

### Right way to write CSS

```CSS
.foo {
    color: whitesmoke;
    border: 1px solid #CCC;
}

.float-left {
    float: left;
}

.one-third {
    width: 33%;
}
```

```HTML
<div class="foo float-left one-third">
    <p>It's even nicer in here.</p>
</div>
```
<table><tr><td><a href="../Chapter-2/README.md">&larr; Previous</a></td><td><a href="../Chapter-3/README.md" >Next &rarr;</a></td></tr></table>
