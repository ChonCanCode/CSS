# CSS Database

## Flexbox

    Flexbox is a layout in CSS allow different row and column to be fitted inside a container element and different shape and form (mixture of row and column orientation). 

    Step 1 - set the display property to flex.
    `display: flex;`
    Step 2 - assign main axis value to the property (changing orientation)
    `flex-direction: column;` or `flex-direction: row;`
    Step 3 - justify-content, align flex items along the main axis of the flex container.
    `justify-content: space-between;`
    Step 4 - align-items items along the cross axis of the flex container.
    `align-items: strectch`
    Step 5 - flex-wrap specify whether flex items should wrap onto multiple lines within a flex container, and how they should behave when wrapping.
    `flex-wrap: wrap`
    Step 6 - flex-grow determines how this space is distributed among the flex items. The available space is divided based on the proportion of the flex-grow values.
    `flex-grow: 1;`
    Step 7 - flex: 1 in CSS is a convenient way to apply flex properties to flex items. It is shorthand for setting the flex-grow, flex-shrink, and flex-basis properties at once.
    `flex: 1;`
    Step 8 - align-self control individual child element, to override the default alignment.
    `align-self: center`


## Selector
    `body {}` This is the CSS selector that targets the <body> element. The styles defined within the curly braces {} will be applied to the <body> of the HTML document.

    `* {}` is called the universal selector in CSS. It selects all elements on the page.

    `.class name {}` In CSS, a "class" refers to a selector that allows you to apply a specific set of styles to HTML elements. Classes are one of the primary ways to target and style elements on a webpage, alongside IDs and tag selectors.

    `#id name {}`id attribute has to be unqiue only 1 per porject

    `footer > section` This selector targets all <section> elements that are immediate children of a <footer> element.

    `header section img {}` targets all <img> elements that are descendants of a <section> element, which itself is a descendant of a <header> element. This means it will apply the specified styles to any <img> elements that are nested within a <section> within a <header>.

    `@media` rule in CSS is used to apply specific styles based on the result of one or more media queries. These queries can target properties such as screen width, height, orientation, resolution, and more. The syntax @media () {} includes a media query condition within the parentheses. If the condition is met, the CSS rules inside the curly braces {} are applied.


## Parameter
    align-items
    justify-content
    `display: flex` is a CSS property used to create a flex container. Flexbox is a layout model     that allows elements within a container to be dynamically arranged based on available space and desired alignment. Here's what display: flex; does and how you can use it:
    

    `align-items: center` is a property used in flexbox layouts to align flex items along the cross axis of the container.

    `justify-content` and `align-items` are often used together to achieve centralized alignment of flex items both vertically (along the cross axis) and horizontally (along the main axis) within a flex container.

    `text-decoration: unset` remove the underline for links button

    `a:hover {}` is a selector and a pseudo-class rule that targets the <a> (anchor) element when it is in a hovered state. 

    `flex: 1` is a shorthand property that is used within a flex container to distribute available space along the main axis of the flex container. Here’s what it does:

    Flex Container Context: The flex property is applied to flex items (child elements) within a flex container (parent element) to control how they grow and shrink to fill the available space.

    Value 1: When you use flex: 1;, you're essentially setting three properties at once:
        flex-grow: 1;: This allows the flex item to grow and take up available space along the main axis of the flex container. The value 1 means it will grow proportionally to other flex items that also have flex-grow specified.
        flex-shrink: 1;: This allows the flex item to shrink if necessary when there is not enough space along the main axis of the flex container. Again, the value 1 indicates it will shrink proportionally to other flex items with flex-shrink specified.
        flex-basis: 0%;: This sets the initial size of the flex item before any remaining space is distributed. The value 0% indicates that the initial size of the flex item is zero percent of the container's main size dimension.
    
    
## Relative Units (em and rem) & Pixel Units (px)

    using em or rem is recommended over px. They offer flexibility, scalability, and better support for responsive and accessible design practices. While px can still be appropriate for certain design elements that require fixed dimensions, it's essential to consider the trade-offs in terms of accessibility and responsiveness when choosing the unit for text sizes in CSS.

    `em` This unit is relative to the font-size of its direct or nearest parent. For text, 1em is equivalent to the font size of the parent element. This makes em useful for creating scalable designs where text sizes adjust proportionally based on the parent element's font size.

    `rem` This unit is relative to the root element (html). Unlike em, which can compound parent element font sizes, rem provides a consistent reference point across your entire document. This makes it particularly useful for maintaining a consistent scale across various elements, especially when dealing with nested elements or complex layouts.