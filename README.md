# Specification of selectors

> My project shows the specificity of styles and their priority based on the style hierarchy.
> [CSS selectors](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors)

In CSS, selectors are used to target the HTML elements on our web pages that we want to style. There are a wide variety of CSS selectors available, allowing for fine-grained precision when selecting elements to style.

> In this project and its sub-articles i will run through the different types in great detail, seeing how they work.

### Specification in my project

- Combinators and separators
  - Next-sibling combinator
    `(div + p)`
  - Child combinator
    `(div > p)`
  - Subsequent sibling combinator
    `(h4 ~ span)`
- Type selectors
  `(<div>, <span>, <p>, <h4>, <a>)`

* Class selectors
  `(.second-paragr, .bgc-div)`
* ID selectors
  `(#link, #id-div, #third-paragr)`

* Attribute selectors
  `([href], [href^="http://"], [href*="ua"], [href$=".pdf"])`

* Combinators
  `(div p, a[href]#link, div.bgc-div#id-div, div p#third-paragr)`

[For a complete list of selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_selectors)

_The table below shows some examples on how to calculate specificity values:_
Selector | Specificity Value | Calculation
:-----|:--------:|------:|
p | 1 | 1
p.class | 11 | 1+10
div p.class | 12 | 1+1+10
div p#id | 102| 1+1+100
a[attr]#id | 111 | 1+10+100
#id | 100 | 100
.class | 10 | 10
div.class#id | 111 | 1+10+100
#id p#id| 201 | 100+1+100

> > There is one exception to this rule: if you use the !important rule, it will even override inline styles!
