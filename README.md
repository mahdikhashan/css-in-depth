# css-in-depth
Practice CSS while reading CSS in-depth book by Keith J. Grant

# Day 1 
- box-model and border-box
- ch-3: column with an adjusted box model now fit side by side
- ch-3: universal border-box fix

add the below CSS style to every new project to have a more predictable box model:

```css
:root {
  box-sizing: border-box;
}

*,
::before,
::after {
  box-sizing: inherit;
}
```

# Day 2
- percentage based gutter (gap) margin
- using calc() to subtract the gutter from the width
- controlling overflow behavior: content overflowing its container 

# Day 3
- equal-height columns with a CSS-based table layout
- negative margins for a corrected gutter

```css
.container {
  display: table;
  width: 100%;
}

.main {
  display: table-cell;
  width: 70%;
}

.sidebar {
  display: table-cell;
  width: 30%;
}
```

# Day 4
- equal height columns using flexbox
- min-height and max-height
- using padding to vertically center contents
- vertical align table cell

reference: http://howtocenterincss.com/#contentType=div&content.width=100px&horizontal=center&vertical=middle&browser.IE=none

# Day 5
  didn't work, off.

# Day 6
  - vertical centring
    - natural height container, apply equal top and bottom padding.
    - need specific height, need to avoid using padding, table-cell and vertical alignment.
    - display flex-box with justify-content.
    - inner content is a one liner, equal height for container and inner content.
    - height of container and inner content is known, then use absolute positioning.
    - unknown inner content height, use absolute positioning in conjunction with a transform.

```css
.content-transform {
  position: relative;
  min-height: 500px;
  border: 1px solid #ccc;
}

.inner-content-for-transform {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: #f00;
  color: #fff;
  padding: 10px;
}
```
# Day 7
  - negative margins

# Day 8
  - margin collapsing part 1

# Day 9
  - didn't work

# Day 10
  - didn't work

# Day 11
  - margin collapsing fix with overflow-auto
  - margin collapsing fix with padding
  - margin collapsing fix with border
  - margin collapsing fix with float
  - margin collapsing fix with inline-block
  - margin collapsing fix with absolute
  - margin collapsing fix with fixed positions
  - margin collapsing fix with flexbox
  - margin collapsing fix with table-cell

# Day 12
  - siblings combinator
  - lobomomized owl selector

```css
/* siblings combinator */
.button-link + .button-link {
  margin-top: 1.5em;
}

/* lobomomized owl selector */
body * + * {
  margin-top: 1.5em;
}
```

# Day 13
  didn't work

# Day 14
  - double container layout, anonymous div for grouping, max-width with margins: 0 auto; for centering
  - container collapsing with floating components, clearfix, ::before, ::after pseudo-elements, clear: both; for height increase to encompass the whole container which has floats, floats don't make parent height increase

# Day 15
  - unexpected float catching

# Day 16
  - media-object

# Day 17
  - attribute selector be like [attribute*="startswith-..."]
  - grid system

```css
[class*="col-"] {
  float: left;
}

.col-1 { width: 8.3333% }
.col-2 { width: 16.6667% }
.col-3 { width: 25% }
.col-4 { width: 33.3333% }
.col-5 { width: 41.6667% }
.col-6 { width: 50% }
.col-7 { width: 58.3333% }
.col-8 { width: 66.6667% }
.col-9 { width: 75% }
.col-10 { width: 83.3333% }
.col-11 { width: 91.6667% }
.col-12 { width: 100% }
```

# Day 18
  - grid columns with gutters

# Day 19
  - flexbox setup, flex container, flex items, main axis, cross axis, autoprefixer