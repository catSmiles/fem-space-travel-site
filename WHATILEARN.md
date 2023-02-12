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

