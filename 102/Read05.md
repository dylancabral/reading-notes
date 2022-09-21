# How To Add CSS\

## There are three ways of inserting a style sheet:

- External CSS
- Internal CSS
- Inline CSS

> External CSS
With an external style sheet, you can change the look of an entire website by changing just one file!
---
`<link rel="stylesheet" href="mystyle.css">`
---
>Internal CSS
An internal style sheet may be used if one single HTML page has a unique style. The internal style is defined inside the `<style>` element, inside the head section.
---
>Inline CSS
An inline style may be used to apply a unique style for a single element. To use inline styles, add the style attribute to the relevant element. The style attribute can contain any CSS property.
---
`<h1 style=color;"blue;text;aligncenter;">`

## Cascading Order

>Cascading Order
What style will be used when there is more than one style specified for an HTML element?
---
>All the styles in a page will "cascade" into a new "virtual" style sheet by the following rules, where number one has the highest priority:
---
>Inline style (inside an HTML element)
External and internal style sheets (in the head section)
Browser default So, an inline style has the highest priority, and will override external and internal styles and browser defaults.

## CSS Color Property

The `color` property specifies the color of text.
---

`body {color: red;}`

---
The `body` signifying which section in html is being affected

---

[Back to Home](../README.md)