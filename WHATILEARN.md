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



