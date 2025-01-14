# Notes for January 11-13, 2025

## Time Tracking

- limited

### HTML & CSS Review

#### Hyper-text

1. Hyper-links make it easy for users to **navigate** from URL to URL. This is what makes normal text into **hyper text** (the H and the T in HTML).
2. Hypertext documents linked to one another is what makes the Web a web. 
3. "Hyperlinks" are also known as "links", a.k.a. `<a>` tags

#### Anatomy of an HTML element

1. **Syntax** is the term for the grammar of a programming language or in this case the markup language, since we are studying HTML
2. Example HTML: `<a href="https://www.wikipedia.org/" target="_blank">Wikipedia</a>`
    1. `<a>` is called the **opening tag** for the anchor element
    2. `</a>` is called the **closing tag** for the anchor element
    3. Everything between the opening tag and closing tag is called the **content**
        1. In this case, Wikipedia.
    4. Within the opening tag (but **never** the closing tag), there might be **attributes**
        1. In this case, there are two attributes:
            - `href="https://www.wikipedia.org/"`
            - `target="_blank"`
        2. Each attribute is comprised of a **name**, then a `=`, then a **value**
            - In this case, `href` and `target` are the **names** of the two attributes
            - `"https://www.wikipedia.org/"` and `"_blank"` are their **values**, respectively
            - **Values** should always be within a pair of quotes ("")
            - We typically don't include spaces around the `=` that connects an attribute's name and value
        3. Within an opening tag, we typically use one space to seperate attributes
3. All of this comes together to create what we call an **element**
4. There are many elements, but all of them have the same structure -- opening tag, closing tag, content, and attributes

#### A very special attribute: style

1. We can use the `style` attribute to change how an element looks.
2. Example: `<a style="color: red" href="https://www.wikipedia.org/" target="_blank">Wikipedia</a>.`
    1. By adding the attribute `style="color: red"`, we have changed the color of the link.
3. Within the value of the `style` attribute, we can write **CSS** (Cascading Style Sheets) -- a whole different language with its own syntax, designed specifically for visual styling.
4. In this **CSS**: `color: red`
    1. `color` is called the **property**
        - CSS offers over 100 properties that you can modify to customize the look and feel of elements
    2. `red` is the **value**
        - For a given property, there is usually a set of valid values that you're allowed to choose from. In this case we're allowed to use the word `red`. There are also many other ways to specify a color
    3. The property must be sepreated from the value by a colon (`:`)
    4. Together, this is one **declaration**
5. You can have multiple declarations within the same `style` attribute, but you must seperate them with a semicolon (;)
    1. Example: `<a style="color: red; font-size: 50px" href="https://www.wikipedia.org/" target="_blank">Wikipedia</a>`
    2. The `font-size` property is how we can change how big text is.
    3. The `px` unit is used to indicate that we want the text to be 50 pixels tall, but there are many other units to specify dimensions.

#### Adding structure with `<span>`

1. If we wanted to change the look of some text that's not within an `<a>` tag, we can wrap the content in a `<span>` element
2. The `<span>` element gives us a hook to hang CSS onto
3. Nothing actually changes when using the `<span>` element until you add the attribute, `style`
    1. Example: `You can <span style="font-style: italic">learn about the world</span>`
4. The `font-style` property is how we choose between normal and italic text.
5. The `<a>` element is purposely built for navigation while the `<span>` element is not clickable
6. `<span>` is used to add *structure* to our content so that we can then style and position bits of it as needed

#### The `<img>` element

1. The `<img>` element allows us to embed images right into our document
    1. The image we want to embed needs to already be on the internet and have its own URL
    2. The URL will be plugged in as the value for the `src` attribute of an `<img>` element to embed it in our page
    3. Example: `<img src="https://upload.wikimedia.org/wikipedia/en/thumb/8/80/Wikipedia-logo-v2.svg/263px-Wikipedia-logo-v2.svg.png">`

#### The HTML family tree

1. Elements can contain other elements
    1. Example: `<span style="color: red">This is the parent element, and <a style="font-weight: bold">this is the child element.</a> Over here I'm back in the parent element.</span>`
    2. The outer element is known as the **parent element**. The inner element is known as the **child element**
    3. One parent element can have multiple children elements
        - If so, the other children of your parent are called sibling elements (like a family tree)
    4. Your children and all of their children, and children's children are called your **descendant elements**
    5. Your parent, parent's parent, etc, are called your **ancestor elements**

#### All whitespace collapses to a single space

1. Despite all the spaces and new lines you can add to the code, the code is **interpreted** and rendered by the browser the same as lines of code that don't have spaces or new lines
2. Whitespace and new lines can't be used to position content around the page where we want it, the way we would in a word processor like Microsoft Word
    1. Tools where the input you create and the output the tool renders are supposed to be the same are called **"What You See Is What You Get"**, or WYSIWYG, also pronounced "wizeewig"
        - Examples include word processors and photoshop

#### Layout systems

1. There are many layout systems provided by HTML. They include:
    1. Flow
    2. Flexbox
    3. Positioned
    4. Grid
    5. Etc.

###### In the beginning, there was Flow

1. The very first layout system offered by HTML was called **flow layout** and for a while, it was the *only* layout system
    1. It makes sense that flow was the first and only layout for a long time, since the earliest use of the web was for scientists to share research papers.
2. In **flow layout**, the browser lays out elements as if it was typesetting a paper book or magazine
3. Words, images, and other **inline** items are placed side by side *horizontally*
4. Paragraphs, headings, and other **blocks** are placed above and below another *vertically*
5. So, in flow layout, if we don't want all of our content to be on the same line, we need to create some elements that act as **block** elements.
    1. By default, `<span>`, `<a>`, and `<img>` elements all act as **inline** elements
6. To make an element act as a **block** instead of **inline**, you need to use the CSS declaration: `display: block`
    1. Example code: `<span style="display: block">Another good place to learn is Khan Academy.</span>`

#### The `<div>` element

1. HTML was merciful and created the **`<div>`** element as a shortcut, so that we don't have to write `<span style="display: block">gibberish</span>` in our `<span>` elements over and over again
2. A **`<div>`** is just a `<span>` with `display: block` already set!
    1. Example code: `<div>Another good place to learn is Khan Academy.</div>`

#### Drawing borders around elements

1. CSS lets us draw boorders around elements
2. Borders make it easier to see where each element is and how much space it's taking up
3. The `border-style` property relates to the style of the border around your element.
    1. The values for the `border-style:` property are `dotted`, `solid`, `dashed`, or `double`.
    2. The default value of `border-style` is `none`
    3. Example code: `<div style="border-style: dotted;">You can learn about the world at Wikipedia.</div>`
4. The default color for borders is whatever color the text of the element is set to
    1. We can customize the color of the border with the `border-color:` property
    2. Example code: `<div style="border-style: dotted; border-color: blue;">You can learn about the world at Wikipedia.</div>`
5. The default width of a border is 1px
    1. We can customize the width of the border with the `border-width:` property
    2. Example code: `<div style="border-style: dotted; border-color: blue; border-width: 10px">You can learn about the world at Wikipedia.</div>`
6. The shortcut for specifying style, color, and width all at once is the `border:` property
    1. You need to input three values. One for style, one for color, and one for width.
    2. Example code: `<div style="border: dotted blue 10px">You can learn about the world at Wikipedia.</div>`
    3. It's much faster and easy to use
7. You can also set the border for each side individually with the `border-top:`, `border-right:`, `border-bottom:`, and `border-left:` properties
    1. Example code: `<div style="border-top: solid blue 10px; border-right: solid red 10px; border-bottom: solid green 10px; border-left: none">You can learn about the world at Wikipedia.</div>`

#### Rounding corners with `border-radius:`

1. You can round the corners of an element using the `border-radius:` property
    1. Example code: `<div style="border: solid blue 10px; border-radius: 10px">You can learn about the world at Wikipedia.</div>`

#### `text-align`

1. We can control the alignment of text within a parent with the `text-align:` property
    1. Example code: `<div style="border: thin red solid; text-align: center">You can learn about the world at Wikipedia.</div>`

#### The box model

1. For elements that are `display: block`, we can set a few useful properties:
    1. `width:` How much space we want the content of the element to take up
    2. `padding:` How much space we want *outside* the content of the element, but *inside* the border
    3. `border:` How much space we want the border to take up
    4. `margin:` How much space we want *outside* the border of the element (between it and its neighbors)
    5. Example code: `<div style="width: 200px; padding: 10px; border: solid red 20px; margin: 30px">You can learn about the world at Wikipedia.</div>`
    6. You can also individually set `padding-top:`, `padding-right:`, `padding-bottom:`, `padding-left:`, `margin-top:`, `margin-right:`, `margin-bottom:`, and `margin-left:`

#### CSS style rules

1. It's common to apply the same set of styles to multiple elements in an HTML document, but repeating the `style="..."` attribute on each element isn't practical
2. CSS provides us with **style rules**
    1. We first need a `<style>` element in our document and then we can write our style rules within that element
3. Example code:

        <style>
            div {
                width: 200px;
                padding: 20px;
                border: solid red 5px;
                margin: 30px;
            }	
        </style>

    1. In this style rule, `div` is called the **selector**
        - This particular selector is saying to target all of the the `<div>` elements in the document
    2. After the selector is a set of curly brackets ({...})
    3. Within the curly brackets, we can have a set of declarations, separated by semicolons (;), just as we could within a `style="..."` attribute
    4. Everything within the curely brackets({...}) is called the **declaration block**
    5. The whole thing all together is called a **style rule**

#### CSS selectors

    <style>
      div {
        width: 200px;
        padding: 20px;
        border: solid red 5px;
        margin: 30px;
      }	

      .danger {
        color: red;
      }
    </style>

    <div>You can learn about the world at Wikipedia.</div>

    <div class="danger">Another good place to learn is Khan Academy.</div>

1. Since `div` is a **tag-type** selector, if we add `color;red;` to the declaration block, it will apply to all `<div>` elements in the document
2. Since the **tag-type** selectore is so broad, we can achieve more precise targeting by dropping back down to the inline style method using the `style="..."` attribute, but you've now lost the ability to affect multiple elements at once with a style rule
3. With a **class-level selector**, we can affect as many elements as we want and they can be different elements like a `<div>` and a `<span>`
    1. In the above example, `.danger` is a class-level selector because we started it with a period(`.`)
    2. To any element we want to apply the style rule to, we must add a `class="danger"` attribute
        - It's important to note that there's no `.` when *applying* a class, only when writing the **selector** (`.danger`)

#### Flexbox layout

1. **Flexbox** is one of CSS' layout systems that makes it easier to put three blocks of text side by side horizontally
2. If you want to change a parent's layout mode too flexbox, we need to use the `display: flex;` declaration
3. Within an element that is `display: flex;`, "block" and "inline" don't really mean anything anymore. These terms are relevant for typesetting, but **flexbox** is for more dynamic, responsive, app-type layouts
4. **Importantly**, `display: flex;` only affects how *immediate children* are positioned within the parent element
    1. The position of the parent element itself and anything outside the parent element is unaffected by setting `display: flex;` on the parent element
5. By default `flex-direction` is `row` (horizontal), but you can also set `flex-direction` to `column`, in which case children will be laid out *vertically* (similar to block layout)
    1. We mostly use flexbox layout when we want to break out of flow layout to achieve horizontal positioning (`row`)

##### justify-content and align-items

1. Using the flexbox layout opens up to us a few new properties, more importantly: `justify-content:` and `align-items`

###### justify-content

1. When `flex-direction:` is `row`, the `justify-content:` property determines how any leftover horizontal space within the parent is used
2. There are five values we can set:
    1. `flex-start`: Place the children on the left side of the parent, and any leftover space on the right. (This is the default value)
    2. `flex-end`: Place the children on the right side of the parent, and any leftover space on the left
    3. `center`: Place the children in the middle of the parent and any leftover space is evenly split across the left and right
    4. `space-between`: Split leftover space evenly between the children -- there's no space on the left or right
    5. `space-around`: Split leftover space evenly between *and* to the left and right of the children

###### align-items

1. When `flex-direction:` is `row`, the `align-items:` property determines how children are placed vertically within the parent
2. There are five values we can set:
    1. `stretch`: Makes children as tall as the parent, so that there is no leftover vertical space. (This is the default value)
    2. `center`: Places children in the middle of the parent and any leftover space is evenly split acorss the top and bottom
    3. `flex-start`: Places the children at the top of the parent and any leftover space on the bottom
    4. `flex-end`: Places the children at the bottom of the parent and any leftover space on the top
    5. `baseline`: Places the children such that the bottom of the text within them is lined up along the center of the parent, regardless of their `font-size`
        - They're useful for things like navigation bars














    
        
