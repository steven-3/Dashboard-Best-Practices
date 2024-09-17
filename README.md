# Dashboard Report Best Practices & Styling Guide

## Best Practices

 1. Set the interactive size of your report to **0in, 0in** \
\
![Screenshot 2024-09-16 174246.png](https://github.com/steven-3/Dashboard-Best-Practices/blob/11261e875df7e0b27fd56ca1b454db67c166bbfa/Screenshot%202024-09-16%20174246.png)

 2. Make sure your parameters are set to **hidden**.\
\
![Screenshot](https://github.com/steven-3/Dashboard-Best-Practices/blob/11261e875df7e0b27fd56ca1b454db67c166bbfa/Screenshot%202024-09-16%20174500.png)

 3. Use the dashboard debugger to see how your report will be viewed in the browser. This site is a guide for determining how wide your reports can be. Height does not matter, but the width will. \
\
![Screnwho2](https://github.com/steven-3/Dashboard-Best-Practices/blob/11261e875df7e0b27fd56ca1b454db67c166bbfa/Screenshot%202024-09-16%20174656.png)

## Report Styling Guide
You can apply basic CSS styling to your report elements using the tooltip property on an element. \
\
![scrensh3](https://github.com/steven-3/Dashboard-Best-Practices/blob/94e695f16197ab72ec34eb19d913ce1ca536c293/Screenshot%202024-09-16%20174933.png)

Here you can see the expression used to apply CSS styling on the rectangle. \
\
![rectangle](https://github.com/steven-3/Dashboard-Best-Practices/blob/94e695f16197ab72ec34eb19d913ce1ca536c293/Screenshot%202024-09-16%20182948.png) 
- The inputted expression is `="CMSTYLE[{style}background-color: black; box-shadow: 10px 5px 5px red;]"`
- Every time you write an expression into the tooltip, you need to start with `=` and use `""`.
- To be able to apply CSS styling you need to put `CMSTYLE` at the beginning to let the program know you will be applying styling to the element.
- HTML elements can have multiple attributes. The program reads from the tooltips expression to apply those attributes onto the element, so to be able to have multiple on this element, we separate each attribute with `[],`.
- In this case, multiple attributes would look like this `="CMSTYLE[{style}background-color: black;],[{title}RECTANGLE]"`.
- As you can also see, to define each attribute you have to put the name of the attribute in curly brackets `{}` at the beginning of each set of brackets `[]`. IE: `[{attribute-name}value]`
- Now going back to the first expression, `="CMSTYLE[{style}background-color: black; box-shadow: 10px 5px 5px red;]"` when inputted into the tooltip, the rectangle will be displayed like below after the report is rendered: \
\
![aferchanges](https://github.com/steven-3/Dashboard-Best-Practices/blob/c5f185429131607ee8afaf96d1ecf29c64b5dd99/Screenshot%202024-09-17%20173753.png)
