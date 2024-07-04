# CSS Database

## Selector
    `body {}` This is the CSS selector that targets the <body> element. The styles defined within the curly braces {} will be applied to the <body> of the HTML document.

    `* {}` is called the universal selector in CSS. It selects all elements on the page.

    `.class name {}` In CSS, a "class" refers to a selector that allows you to apply a specific set of styles to HTML elements. Classes are one of the primary ways to target and style elements on a webpage, alongside IDs and tag selectors.

    `#id name {}`id attribute has to be unqiue only 1 per porject


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