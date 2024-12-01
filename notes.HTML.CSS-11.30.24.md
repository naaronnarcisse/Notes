
# Notes for November 30, 2024

## Time Tracking

- 8:00 PM to 10:00 PM: Continue HTML and CSS crash course on Scrimba

## anchors and attributes

### The `<a>`

1. Short for "anchor"
2. Used to **link** either to a different location within the current page or to another paged

### Attributes

#### Elements can have attributes

1. **Attributes are always within the opening tag**
2. Attributes give **extra information** to the browser about that element, such as where a link goes, or the location of an image file
3. Attributes are **normally** followed by an equal sign and quotation marks
    1. Ex. `<a href="https://google.com">google</a>`
    2. So, when you click on the word google, it will send you to the link in the `href` attribute
4. Some elements *require* an attribute
    1. A link will **not** work without an href attribute

### Links

#### Absolute paths

1. If the page you are linking to is **NOT** part of your website, **it MUST start with http:// or https:// to let the browser know it is an external site that you are linking to

#### Relative paths

1. You can link to other pages within your site by simply putting their file name
    1. Ex. Visit our `<a href="about-us.html">about us</a>` page!
    2. Ex. Visit our `<a href="team/john.html">about us</a>` page!

## Intro to CSS

1. CSS is all about **property:value
** pairs

### Properties

1. Properties are what we want to change
    1. color
    2. font-size
    3. font-weight

### Values

1. Values are what we want to set that property to
    1. font-size: 21px;

### The syntax

1. There must be a colon (:) between the property and the value
2. There must be a semicolon (;) after the value
    1. font-size**:** 21px**;**

### The style attribute

1. There's a few ways to add CSS to an HTML document, but for now we will use **inline** CSS by using the *style* attribute.
    1. Ex. `<p style=" ">`
    2. We can write CSS inside the quotation marks.
    3. This *style* attribute is similar in format to the href attribute of the `<a>`

#### Recap

1. CSS is written in property: value pairs
2. They are always seperated by a colon (:)
3. The value is always followed by a semicolon (;)
4. We can write CSS inside a *style* attribute

## CSS Basics

### Some basic styles

1. font-size - Sets the font size. 
    1. There are different units you can use, but for now let's stick to **px** (pixels)
2. color - Changes the color of the text
3. background-color - Sets the background color
4. text-align - Align the text to the **left**, **center**, or **right**

#### More about color

1. Colors can be set with keywords, hex codes, rgb and hsl values
    1. keywords - "red", "steelblue", "hotpink"
    2. hex - hexadecimal values - ex. #7ab0fb
        1. Sometimes called hex codes
        2. It's always a hastag followed by six letters or numbers
        3. The letters go from a to f and the numbers go from 0 to 9
        4. It's an RBG system
    3. rgb - Red, Green, Blue - ex. rgb(0, 255, 0)
        1. The scale goes up to 255, so in this example we see it's 100% green
    4. hs1 - Hue, Saturation, Lightness - ex. hs1(240, 100%, 75%)