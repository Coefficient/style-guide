# HTML Style Guide

1. Favor Classes over ID's for markup you intend to style.
2. ID's should only be used under the following circumstances:
  * Performance implications
  * 3rd party library requires it
3. Use 4 spaces per tab.
4. Use .html extension.
5. ~~Try to prefix all javascript-based selectors with `js-`. This is taken from [slightly obtrusive javascript](http://ozmm.org/posts/slightly_obtrusive_javascript.html). The idea is that you should be able to tell a presentational class from a functional class. Although we are moving towards a one page app with AngularJS, and this point becomes moot, some of the codebase still uses jQuery.~~ This is moot now that we are an SPA.

### Wrong way to write HTML

```HTML
<div id="foo"><p>What a terrible place to be</p></div>
```

### Right way to write HTML

```HTML
<div class="foo bar">
    <p>What an interesting place to be.</p>
</div>
```

<table><tr><td>&larr; Previous</td><td><a href="../Chapter-2/README.md" >Next &rarr;</a></td></tr></table>
