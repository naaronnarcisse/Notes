# Notes for January 8, 2025

## Time Tracking

- 7:00 PM to 9:00 PM: Continue HTML and CSS crash course on Scrimba

### Basic Layout Practice Page

#### Important things picked up while working on the page

1. In CSS, any value that is 0 doesn't need a label like "px" because 0 will remain 0. 
    1. For exmaple, instead of `padding: 25px 0px;`, you can do `padding: 25px 0;` and it will mean the same thing.

#### Centering an element on the page

1. Margins accept a set width, but you can also use the **auto** keyword
    1. **Auto** will automatically place all the available space on that side
    2. If we use **auto** on both the left and the right, it will center the element on the page 
    - Ex. `margin: 0 auto;`
    3. This won't work on the top and bottom to center vertically. A margin top and bottom of auto will just default to zero.
2. The long strip of margin on both sides of the page that doesn't allow for anything (text, color, etc.) to touch it can be turned off.
    1. To do this, you need to go into the body itself and give the margin a value of 0.
    - Ex. `margin: 0;`

#### Creating columns using flexbox

1. For the longest time, we had to use something called floats to make block level elements go next to one another, but it wasn't made for layouts
2. It involved things sliding under the other and clears
3. **Flexbox** is our first layout tool
    1. By default, when setting **`display: flex;`** on an element in CSS, all the children of the element will become columns
4. Unlike `<main>`, **`<div>`** has no meaning, so we can give them class names, so we know what we're using them for
    - Ex. `<div class="column">`
5. Use comments because they can help you out by keeping you organized and to know where you are in your code
    1. Tip: You can use them at the end of a closing `</div>` tag to help you know which `<div>` it belongs to
6. When you have elements that all have the same class name, whenever you go to change that class, it effects everything that falls under that class name
7. Don't be afraid to add empty space to your code
8. Things that deal with text in general flow through flow through all the text, including the children of that element

