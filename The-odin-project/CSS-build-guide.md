# CSS Build Guide

## Basic Syntax
- CSS is made up of various rules. These rules are made up of a selector.

```
div.bold-text {
//^ Selector
    font-weight: 700;
    //^ property //^ value
}
```

## Selectors
- Class selector - can apply style to multiple elements in HTML. and within HTML a single class attribute can have multple classes selected mention within as below.
- ID selector - can only have one ID. It cannot be repeated on a single page and should not contain any space within the attribute. 


```
HTML
<div class"iAmClass"></class>
<div id="iAmId iAmIdTwo"></div>

CSS
.iAmClass,
.iAmClassTwo {
    color:red;
}

#iAmId {
    color:black;
}
```

## Chaining selectors
- Chaining Class and Class Selectors
The selector .subsection.header targets elements that have both the subsection and header classes. In the given HTML, this applies to the first <div> with the content "Latest Posts". The style rule sets the text color of this element to red.

- Chaining Class and ID Selectors
The selector .subsection#preview targets an element with the class subsection and the ID preview. In the HTML example, this applies to the <p> element. The CSS rule sets the text color of this element to blue.

```
HTML
<div>
  <div class="subsection header">Latest Posts</div>
  <p class="subsection" id="preview">
    This is where a preview for a post might go.
  </p>
</div>

CSS
.subsection.header {
  color: red;
}

.subsection#preview {
  color: blue;
}
```

## Descendant combinator
- To combine multiple selectors differently than either grouping or chaining them. In the following example only (B & C) will be selected

```
HTML
<div class="ancestor">
  <!-- A -->
  <div class="contents">
    <!-- B -->
    <div class="contents"><!-- C --></div>
  </div>
</div>

<div class="contents"><!-- D --></div>

CSS
.ancestor .contents {
  /* some declarations */
}
```

## Cascading in CSS
- Refers t othe way in which styles are applied to elements on a webpage, based on a set of rules that determine how styles are combined and priortised. It inovles three main aspects.
1. Inheritances - Certain CSS properties can be interited from parent to child. Not all properties are inheritable; e.g. `margin` and `padding`.
2. Specificity - Determine which stytles are applied by ranking rules based on their selectors. The more specific the higher the ranking.
  - Inline Stylees (e.g., `<div style="color: red;">`)` in HTML
  - ID selectors (e.g. `#iAmID`) highest specificity
  - Class selectors (e.g. `.iAmClass`), Attribute selectors (e.g. `[type="text"]`), Pseudo-classes(e.g. `:hover`) have lower specificity
  - Type selectors (e.g. `p`,`div`) and Pseudo-elements (e.g. `::hover`) have the lowest specificity

## CSS the boxing model
- Every single thing on a webpage is a rectangular box. These boxes can have other boxes in them and can sit along side one another.

```
+------------------+   +------------------+
|      Box 1       |   |      Box 2       |
|  +------------+  |   |  +------------+  |
|  |  Box 1.1   |  |   |  |  Box 2.1   |  |
|  +------------+  |   |  +------------+  |
|  +------------+  |   |  +------------+  |
|  |  Box 1.2   |  |   |  |  Box 2.2   |  |
|  +------------+  |   |  +------------+  |
+------------------+   +------------------+
```
### Box manipulation
- `padding` adds space inside the border, between the border and content. it affects the size of the element's box and pushes the conten away from the border.
- `border` the boundary of the element's box. It affects the element's dimensions and can be styled in various ways (e.g. solid, dashed, doteted).
- `margin` affects the spacing between elements and pushes other elements away. It is outside the border and can collapse with adjacent margins.
- `Outline` provides a visual cue around the element does not affect the document layout.

```
+-----------------------------+
|          Margin             |  <-- Space outside the border
+-----------------------------+
| +-------------------------+ |
| |       Border            | |  <-- Defines the boundary of the box
| | +---------------------+ | |
| | |     Padding         | | |  <-- Space inside the border
| | | +---------------+ | | | |
| | | |   Content     | | | | |
| | | +---------------+ | | | |
| | +---------------------+ | |
| +-------------------------+ |
+-----------------------------+

```

## Block and Inline
- `display:block` default style type wher elements will be stacking atop each other, each new element starting on a new line.
- `display:inline` appear in line with whatever elements they are plced beside. 

## Divs and Spans
- `<divs>` are block-element by defualt & `<spans>` are inline-level element by default these are just generic boxes that cna contain anything. Two most common usage:
  - Hook element, giving class and id for stylin
  - Grouping element, under one parent element to correctly position them on the page.

## Boxstyling
- Property `border-radius: 24px` controlling the shape of the edge of the corner. 

## Flexbox
- Property `display: flex`
- Property `flex-grow: <num>` control how much a flex itemshould grow relative to other flex items inside the same container and how the remaining space in the flex container is distrubited among the flex items. The space is distrubited based on the relative value of `flex-grow` compared to other flex items.
- Property `flex-shrink: <num>` control how much space to shrink if there is not enough space ine the flex container. 
- Property `flex-base: <num>` control the initial size of a flex item before any available space is distributed `flex-grow` or before any space is removed `flex-shrink`.
- Property `flex-direction: row/column` control which direction does the elements lining vertically or horizontally.
- Property `flex-base: <num>`control the initial size of a flex item before any available space is distributed `flex-grow` or before any space is removed `flex-shrink`.
- Property `justify-content:`
- Property `align-item: `
- Property `aspect raio: 1/1` ensure the elements scale proportionally across different screen sizes & devices.
- Property `height:` & `width:` control how tall/wide the element wil be.
 - `height: auto`
 - `height: 50%`
 - `min-height: 130px`
 - `max-height: 240px`
 - `height: initial `
 - `height: 50vh/vw`
 - `height: Unset`
 - `height: inherit`
 - `height: content-box/border-box`
- Property `align-self:` override the `align-items` property for a specific flex item within a flex container. Allow a single flex item to move corss axis.
- Property `order:<num>` control the order of flex items within a flex container. Affects the visual order of items without changing their actual position in HTML. By defualt all order has a `0` value. In the even the values are even it will be priortised by the order from HTML. 