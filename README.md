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