
# Notes for December 5, 2024

## Time Tracking

- 6:30 PM to 9:20 PM: Continue HTML and CSS crash course on Scrimba

## Recap of all we've learned so far

### The building blocks of the web

1. HTML
2. CSS
3. Jvascript

### HTML

1. **H**yper**T**ext **M**arkup **L**anguage
2. The content of websites
3. Relatively straight forward
4. If you only use HTML, you have a functioning web page

#### Basic file structure for HTML

    <!DOCTYPE html>
    <html>
        <head>
            <title>page title</title>
        </head>
        <body>
        Content goes here
        </body>
    </html>

#### Elements can have attributes

1. Attributes are always within the opening tag
2. Attributes give **extra information** to the browser about that element, such as where a link goes, or the location of an image file
3. Attributes are normally followed by an equal sign and quotation marks 
    1. `<a href="https://google.com">google</a>`

### CSS
1. **C**ascading **S**tyle **S**heets
2. How our websites look
    1. Fonts, colors, backgrounds, layouts, and more
3. Without CSS, websites would look pretty boring
4. CSS is all about **property: value;** pairs
    1. **Properties** are what we want to change
        1. color
        2. font-size
        3. font-weight
        4. text-align
        5. background-color
    2. **Values** are what we want to set that property to
        1. font-size: **21px**;
5. There must be a colon (:) between the property and value
6. There must be a semicolon (;) after the value

#### The style attribute

1. To add CSS using the inline styling method, you need to use the **style** attribute
    1. `<p style="font-size: 21px;">`
    2. We can write CSS inside the quotation marks

### Lists

1. Lists are used for all sorts of things
    1. Regular bullet and numbered lists
    2. Navigations
    3. Organizing other content
2. Two types of lists
    1. Ordered lists **`<ol>`**
        1. Ordered lists are numbered lists
    2. Unordered lists **`<ul>`**
        1. Unordered lists are bullet lists
3. Inside of our lists, we need to use **list items**
    1. Each bullet or numbered item is a list item **`<li>`**

#### Example code for an ordered list `<ol>`

    <ol>
        <li>list item</li>
        <li>list item</li>
        <li>list item</li>
    </ol>

### Images 

1. Images are like links, in that **they require an attribute to work**.
2. A link uses the *href* attribute to link to another file.
3. Images use the **src** attribute which is short for **source**.

#### Images - the syntax

1. `<img src="image.jpg">`
    1. The **img** is the tag itself
    2. **src** is our source attribute
    3. In the quotation marks, we need to put the file name for our image.
2. Images are different from other elements, in that they are **self-closing** 
    1. `<img src="image.jpg">` and `<img src="image.jpg" />` are both valid tags
    2. The latter used to be required to indicate that the `<img>` tag is self-closing, but now it is up to personal preference since the requirement has been removed by HTML5

#### File path

1. Like links, we can point to external images by including the entire URL of the image (http:// or https://), or we can point to images within our site by listing the file name
    - Ex. `<img src="image.jpg">`
    - Ex. `<img src="https://website.com/image.jpg">`
2. It is generally considered bad practice to link off to external sites
    1. Some sites will even block you from being able to do that because it uses up their bandwidth, so it is possible that they will give you a placeholder instead

#### Images - the syntax continued

1. Images are not valid without an **alt** attribute
2. The alt attribute is used to describe the image
3. The alt attribute is short for **alt text** or **alternative text**
4. The main reason it's used is for accessibility reasons, so people who are blind or have bad vision, can use screen readers that read the website to them.
    1. If you don't include the alt attribute then the person won't know what the image is
    - Ex. `<img src="cute-cat.jpg" alt="a very cute cat">`
5. The alt text should describe the intent of the image and not just what the image is
6. If it is a decorative element or logo, it doesn't need alt text (but it *does* still require the alt attribute)
    - Ex. `<img src="logo.jpg" alt="">`
    - Ex. `<img src="decorative-red-ball.jpg" alt="">`


