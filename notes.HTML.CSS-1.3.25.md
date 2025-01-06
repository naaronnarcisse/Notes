# Notes for January 3, 2025

## Time Tracking

- 7:00 PM to 9:00 PM: Continue HTML and CSS crash course on Scrimba

## HTML and CSS

### Necessary Tags (for now)

1. The tags we've learned so far have nothing to do with building a layout, but instead have to do with putting context on a page
    1. h1 -> h6
    2. p
    3. strong and em
    4. a
    5. ul, ol, and li
    6. img

#### Building Layouts

1. There are several "layout" related HTML elements.
2. They all function in the same way, so once you understand how one workds, you understand how they all work
3. The difference between them is that they denote different parts of your website
    - Examples include:
    1. header
    2. main
    3. section
    4. footer
    5. nav
    6. div (**generic box**)
    7. etc
4. Most of the elements were introduced after HTML5, but the **div** has been there since before that
5. All these elements make boxes on our pages

### The Box Model

1. Most elements are **block level** elements by default
    1. They have a width of 100% of their parent
    2. They have a height of 0
    3. The height grows to match the content
        1. Try to **avoid** setting height because, again, height grows to match the content
        2. It's a common problem to have your content overflowing to the point where it overlaps with other content
    4. They stack one on top of the other
    5. We can control the width and height of elements

### The Box Model - Margins & Padding

#### Margins

1. **Margins** are used to control the position of an element relative to those around it (meaning it controls the space around an element)
    1. We can do this with four different properties
        - margin-left
        - margin-right
        - margin-top
        - margin-bottom
2. We also have a **shorthand margin property**
    1. You just write "margin" without specifying top, bottom, left, or right
    2. You can include up to four different values for the margin properties 
    - Ex. `margin: 10px 20px 30px 40px`
    3. Each value stands for the position it affects
        1. The first value, 10px, affects the **top** margin
        2. The second value, 20px, affects the **right** margin
        3. The third value, 30px, affects the **bottom** margin
        4. The fourth value, 40px, affects the **left** margin
    4. The order of these values makes sense when you realize it's going clockwise
    5. We can use one, two, three, or four values in the shorthand margin property
        1. If you only include one value, it's going to apply that value to all four sides
        - Ex. `margin: 10px;`
        2. If you include two values, the first value will be your top and bottom and the second value will be your left and right
        - Ex. `margin: 10px 20px;`
        3. If you include three values, the first value will be the top, the second value will be right and left, and the third value will be bottom
        - Ex. `margin: 10px 30px 40px;`

#### Padding

1. Padding is used to control the positioning of content *inside* our element
2. It works just like margin in terms of the long form and shorthand properties
- Ex. of long form `padding-top: 20px;`
- Ex. of shorthand `padding: 20px 30px 40px 50px;`
3. Background is necessary to see the effects of padding

### Recap on Margins & Padding

1. Margin adds empty space to the outside (margin = empty space)
2. Padding adds empty space to the inside (padding = more background)

### The Box Model - Borders

1. Borders add a border around your element. They are similar to a stroke if your are used to vector software.
2. **It takes three properties to set a border**
    1. border-width
        - It's in pixels, for example, 20px
    2. border-style
        - 99% of the time, it's going to be solid, but there are other values you can use
    3. border-color
3. We can also use border shorthand (The order you put them in doesn't matter)
    - Ex. `border: 2px solid skyblue;`
    1. If you don't add a color, it will default to the color of the text
    2. If you don't add a style or width, the border won't be created
4. You can control the border of all four sides independantly of one another by specifying border-left, border-right, border-top, and border-bottom
    1. You can control side even with a base style, width, and color for the border. For example:
        border: 10px solid red;
        
        border-bottom-color: yellow; 
        border-left-style: dashed;   
        border-right-width: 40px;

### The Box Model - Wrap Up

1. The total width and height of an element is calculated by adding all different parts of the element together
2. **The four parts of an element**
    1. The content itself (what you set the width & height on)
    2. The padding (background or space around our element)
    3. The border
    4. The margin (space outside the element)
3. Don't forget that margin, padding, and borders add width to the left and the right side