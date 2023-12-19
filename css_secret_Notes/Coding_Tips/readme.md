### Minimize Code duplication 
### When values depen on each other , try to reflect their relationship in the code
For example: for Button
```
padding: .3em .8em;
border: 1px solid #446d88;
background: #58a linear-gradient(#77a0bb, #58a);
border-radius: .2em;
box-shadow: 0 .05em .25em gray;
color: white;
text-shadow: 0 -.05em .05em #335166;
font-size: 125%;
line-height: 1.5
```
Here we wanted our font size and measurements to be relative to the parent font size, so we used ems. In some cases, you want them to be relative to the root font size (i.e.,the font size of <html>), and ems result in complex calculations. In that case, you can use the rem unit. Relativity is an important feature in CSS, but you do have to think about what things should be relative to.

### Maintainablility versus Brevity
Consider the following snippet to create a 10px thick border on every side of an element, except the left one:
`border-width: 10px 10px 10px 0`

It’s only one declaration, but to change the border thickness we would need
to make three edits. It would be much easier to edit as two declarations,
and it’s arguably easier to read that way too:
`border-width: 10px;`
`border-left-width: 0`

■ Use percentages instead of fixed widths. When that’s not possible, use viewport-relative units (vw, vh, vmin, vmax), which resolve to a fraction of the viewport width or height.
■ When you want a fixed width for larger resolutions, use max-width, not width, so it can still adapt to smaller ones without media queries.
■ Don’t forget to set a max-width of 100% for replaced elements such as img, object, video, and iframe.
■ In cases when a background image needs to cover an entire container, background-size: cover can help maintain that regardless of said
container’s size. However, bear in mind that bandwidth is not unlimited, and it’s not always wise to include large images that are going to be scaled down via CSS in mobile designs
■ When laying out images (or other elements) in a grid of rows and columns,
let the number of columns be dictated by the viewport width. Flexible Box
Layout (a.k.a. Flexbox) or display: inline-block and regular text wrapping can help with that.
■ When using multi-column text, specify column-width instead of column-count, so that you get one column only in small resolutions.




