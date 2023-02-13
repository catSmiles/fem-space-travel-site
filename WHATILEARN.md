### How the em unit works
The "em" unit in CSS is a relative unit of measurement that is based on the font-size of the element. An "em" unit is equal to the font-size of the element it is applied to. If the font-size of an element is 16px, then 1em is equal to 16px.

Here's an example of how to use the "em" unit in CSS:

   p {
     font-size: 16px;
     line-height: 1.5em;
   }

In this example, the font-size of the p element is set to 16px, so the line-height is 1.5 * 16px = 24px. This means that the height of each line of text in the p element will be 24px.

The "em" unit can be useful for creating scalable and responsive designs because it adjusts based on the font-size of the element it is applied to. For example, if you increase the font-size of the p element to 18px, the line-height will automatically adjust to 1.5 * 18px = 27px.

### How the minmax() Function works

The minmax() function in CSS is used to specify the size range for a grid item or other flexible box elements, such as columns or rows. The function takes two values as arguments: a minimum value (min) and a maximum value (max).

The min value specifies the smallest size that the element can be, while the max value sets the upper limit of the size. The actual size of the element will be determined by the size of its parent container and the values of min and max.

For example, consider the following CSS code:

   .grid-container {
     display: grid;
     grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
   }

In this code, the grid columns have a minimum width of 200px and can take up a maximum of 1 fraction unit of the grid container's available space. If the grid container is 800px wide, then each column will be at least 200px wide, and the total number of columns will be determined by dividing the container width by the minimum column width.

The minmax() function is particularly useful for creating responsive designs, as it allows you to set a minimum size for an element while also allowing it to grow or shrink as necessary based on the available space. This makes it easier to create flexible, scalable layouts that adapt to different screen sizes and orientations.

Link description: https://bitsofco.de/how-the-minmax-function-works/

### How the clamp() Function works

The "clamp()" function in CSS is a relatively new function that allows you to specify a range of values for a property, similar to the "minmax()" function. However, the "clamp()" function provides a more flexible way to set ranges, as it allows you to specify three values instead of just two.

The "clamp()" function takes three arguments: a minimum value, a preferred value, and a maximum value. If the preferred value is within the specified range, it will be used as the value of the property. If the preferred value is outside of the range, the minimum or maximum value will be used instead, depending on which value is closer to the preferred value.

Here's an example of how to use the "clamp()" function in CSS:

    .element {
      font-size: clamp(12px, 2vw, 18px);
    }

In this example, the font-size of the .element will be set to 2vw, as long as the resulting size is between 12px and 18px. If the calculated size is less than 12px, the font-size will be set to 12px. If the calculated size is greater than 18px, the font-size will be set to 18px.

The "clamp()" function provides a more flexible way to set ranges for CSS properties, as it allows you to set a preferred value that can be overridden if necessary to meet the specified range. This can be useful for ensuring that text remains legible on different screen sizes, for example.

Note that using clamp() for font sizes, as in these examples, allows you to set a font-size that grows with the size of the viewport, but doesn't go below a minimum font-size or above a maximum font-size. It has the same effect as the code in Fluid Typography but in one line, and without the use of media queries.

### How the max() Function works

In CSS, the max function can be used to specify the maximum value for a property. The max function takes one or more values as arguments and returns the highest value of those arguments. For example:

    .element {
      width: max(500px, 90%);
    }

In this example, the width property of the .element class will be set to 500px if the parent container is narrower than 500px, and 90% if the parent container is wider than 500px.

The max function can be used with any property that accepts a length, percentage, or number value. For example, you could use max to set the height of an element:

    .element {
      height: max(300px, 20%);
    }

In this case, the height of the .element class will be set to 300px if the parent container is shorter than 300px, and 20% if the parent container is taller than 300px.

### What is the inset CSS property

The inset CSS property is a shorthand that corresponds to the top, right, bottom, and/or left properties. It has the same multi-value syntax of the margin shorthand.

Definition and Usage
 - The inset property sets the distance between an element and the parent element.

The inset property is a shorthand property for the following properties:
   + top
   + bottom
   + left
   + right

Links description:
 - https://www.w3schools.com/cssref/css_pr_inset.php
 - https://developer.mozilla.org/en-US/docs/Web/CSS/inset

### How to min() Function works

The min() function in CSS is a mathematical function that returns the minimum of two or more values. It is part of the CSS Calc() function, which allows you to perform calculations in CSS to determine values for CSS properties.

Here's an example of how to use the min() function in CSS to set the width of an element:

    div {
      width: min(50%, 500px);
    }

In this example, the min() function is used to set the width of the div element to either 50% of the parent element's width or 500 pixels, whichever is smaller.

The min() function can be useful in responsive design, as it allows you to set a limit on the size of an element, regardless of the size of the parent element. For example, you could use the min() function to ensure that a text area never becomes smaller than a certain size, regardless of the size of the viewport.

It's important to note that the min() function can only be used with CSS Calc(). This means that you cannot use the min() function on its own, but must use it in conjunction with other CSS properties and values.

### What is backdrop-filter?

The backdrop-filter property in CSS is used to apply graphical effects (such as blur or color adjustment) to the area behind an element. The backdrop-filter property applies effects to the entire element, including any parts of the element that are transparent.

Here's an example of how to use the backdrop-filter property in CSS to blur the area behind an element:

    div {
      backdrop-filter: blur(10px);
    }

In this example, the backdrop-filter property is used to apply a 10 pixel blur to the area behind the div element.

It's important to note that the backdrop-filter property is not supported by all browsers and may require vendor prefixes for cross-browser compatibility. Additionally, the performance of the backdrop-filter property may be poor on older devices, so it's important to use it judiciously.

Links description:
 - https://www.w3schools.com/cssref/css3_pr_backdrop-filter.php
 - https://developer.mozilla.org/en-US/docs/Web/CSS/backdrop-filter

### what is @media (hover: hover)

`@media (hover: hover)` is a media query in CSS that checks if the user's device has a hover capability, such as a mouse, trackpad, or touch screen with hovering capabilities. This media query allows you to apply specific styles only when the user is hovering over an element with a mouse or other device that provides hover capability.

Here's an example of how to use the @media (hover: hover) media query in CSS:

    @media (hover: hover) {
      a:hover {
        color: red;
      }
    }

In this example, the @media (hover: hover) media query checks if the user's device has hover capability. If it does, the styles inside the media query will be applied, making the text color of an a element red when the user hovers over it with a mouse or other device that provides hover capability.

It's important to note that the @media (hover: hover) media query is not supported by all browsers and may require vendor prefixes for cross-browser compatibility. Additionally, devices without hover capabilities, such as touch screens, will not apply the styles specified in the media query.


### what is @supports (backdrop-filter: blur(1rem))

The @supports CSS directive allows you to apply styles only if a specific CSS property and value are supported by the user's browser. The directive is used to test for CSS feature support, and styles within the directive will only be applied if the property and value are supported.

In the case of @supports (backdrop-filter: blur(1rem)), the @supports directive is checking if the backdrop-filter property with a value of blur(1rem) is supported by the user's browser. If it is supported, the styles within the directive will be applied. If it is not supported, the styles will be ignored.

Here's an example of how to use the @supports (backdrop-filter: blur(1rem)) directive in CSS:

    @supports (backdrop-filter: blur(1rem)) {
      div {
        backdrop-filter: blur(1rem);
      }
    }

In this example, the @supports directive is checking if the backdrop-filter property with a value of blur(1rem) is supported. If it is, the backdrop-filter property will be applied to a div element with a blur of 1 rem. If it is not supported, the styles within the @supports directive will be ignored.

It's important to note that the @supports directive is a relatively new CSS feature, and may not be supported by older browsers. Additionally, the backdrop-filter property is not supported by all browsers, so it's important to check for support before using it in your styles.

### what is aspect-ratio CSS

Aspect ratio in CSS refers to the proportional relationship between the width and height of a rectangular element, such as an image or a video. In CSS, aspect ratio can be controlled using padding and a container element with a fixed width.

Here's an example of how aspect ratio can be controlled using CSS:

    .container {
      width: 500px;
      height: 0;
      padding-bottom: 20%;
    }

    .element {
      width: 100%;
      height: 100%;
    }

In this example, the .container element has a fixed width of 500px, and the padding-bottom property is set to 20%. This means that the height of the container will be 20% of its width, resulting in an aspect ratio of 5:1 (width to height). The .element element inside the container will take up the entire container and maintain the aspect ratio.

Note that this method of controlling aspect ratio only works for a single fixed aspect ratio, and you need to adjust the padding-bottom value to change the aspect ratio. To support multiple aspect ratios, you can use JavaScript or use modern CSS techniques like grid and object-fit.

Definition and Usage
 - The aspect-ratio property allows you to define the ratio between width and height of an element.

 - If aspect-ratio and width properties are set, the height will follow in the defined aspect ratio.

 - To better understand the aspect-ratio property, view a demo.

 - Tip: Use the aspect-ratio property in responsive layouts where elements often vary in size and you want to preserve the ratio between width and height.


### order in Flex CSS?

The order property in CSS Flexbox is used to specify the order of elements within a flex container. By default, elements in a flex container are arranged in the order they appear in the HTML document. However, you can use the order property to change this order.

Here's an example:

    .container {
      display: flex;
      flex-direction: row;
    }

    .element-1 {
      order: 2;
    }

    .element-2 {
      order: 1;
    }

In this example, .element-1 will be displayed after .element-2, even though .element-1 appears first in the HTML. The order property takes a numerical value, where elements with lower values are displayed first, and elements with higher values are displayed last.

### @media (min-width: 35em) and (max-width: 45em)

The CSS media query @media (min-width: 35em) and (max-width: 45em) specifies that the styles inside the media query will only be applied when the viewport (or screen) width is between 35 and 45 ems.

em is a relative unit of measurement in CSS, which is based on the font size of the parent element. In this case, if the font size of the parent element is 16px, 1em is equal to 16px.

So, 35em is equivalent to 560px (35 * 16) and 45em is equivalent to 720px (45 * 16). Therefore, the styles inside this media query will only be applied when the viewport width is between 560px and 720px.

This media query can be useful for creating responsive designs and adjusting the layout and styling of a website based on the screen size of the device being used to view it.

### @media (min-width: 35em)

The CSS media query @media (min-width: 35em) specifies that the styles inside the media query will only be applied when the viewport (or screen) width is 35 ems or greater.

em is a relative unit of measurement in CSS, which is based on the font size of the parent element. In this case, if the font size of the parent element is 16px, 1em is equal to 16px.

So, 35em is equivalent to 560px (35 * 16). Therefore, the styles inside this media query will only be applied when the viewport width is 560px or greater.

This media query can be useful for creating responsive designs and adjusting the layout and styling of a website based on the screen size of the device being used to view it. For example, you can use this media query to apply styles for larger screens, such as desktop computers, and make sure that these styles are not applied to smaller screens, such as smartphones.

### @media (max-width: 45em)

The CSS media query @media (max-width: 45em) specifies that the styles inside the media query will only be applied when the viewport (or screen) width is 45 ems or less.

em is a relative unit of measurement in CSS, which is based on the font size of the parent element. In this case, if the font size of the parent element is 16px, 1em is equal to 16px.

So, 45em is equivalent to 720px (45 * 16). Therefore, the styles inside this media query will only be applied when the viewport width is 720px or less.

This media query can be useful for creating responsive designs and adjusting the layout and styling of a website based on the screen size of the device being used to view it. For example, you can use this media query to apply styles for smaller screens, such as smartphones, and make sure that these styles are not applied to larger screens, such as desktop computers.

### what is margin-block CSS

The margin-block CSS property sets the margin on the block-start and block-end sides of an element. It is used to specify the space outside an element, on the top and bottom of the element.

The margin-block property is part of the CSS Box Model, which defines the layout and positioning of elements on a web page. The Box Model consists of four components: the content, padding, border, and margin. The content of an element is surrounded by the padding, which is surrounded by the border, which is surrounded by the margin.

The margin-block property can be set using a length, percentage, or one of the following keywords:

auto: sets the margin to an automatically calculated value, usually to center an element horizontally within its container
inherit: inherits the value from the parent element
Here's an example of how you can use the margin-block property:

    p {
      margin-block: 20px;
    }

In this example, a 20px margin is set on the top and bottom of every <p> element.

### what is padding-inline CSS

The padding-inline CSS property sets the padding on the inline-start and inline-end sides of an element. It is used to specify the space inside an element, on the left and right of the element.

The padding-inline property is part of the CSS Box Model, which defines the layout and positioning of elements on a web page. The Box Model consists of four components: the content, padding, border, and margin. The content of an element is surrounded by the padding, which is surrounded by the border, which is surrounded by the margin.

The padding-inline property can be set using a length, percentage, or one of the following keywords:

auto: sets the padding to an automatically calculated value, usually to center an element horizontally within its container
inherit: inherits the value from the parent element
Here's an example of how you can use the padding-inline property:

    p {
      padding-inline: 20px;
    }

In this example, a 20px padding is set on the left and right of every <p> element.

Note: The padding-inline property is not a standard CSS property and may not be supported by all browsers. To specify padding on the left and right sides of an element, you should use the padding-left and padding-right properties instead.



