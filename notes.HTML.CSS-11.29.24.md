
# Notes for November 29, 2024

## Time Tracking

- 8:00 PM to 11:00 PM: Continue HTML and CSS crash course on Scrimba

### The `<body>`

1. This is the part that is visible to a user when they visit a page

#### Headings within the body

1. Headings denote hierarchy and page structure
2. Six levels of headings (`<h1>, <h2>, <h3>, <h4>, <h5>, and <h6>`)
3. The headings stop at `<h6>`!
4. Every webpage has one `<h1>` heading and the other levels of heading are used more frequently throughout the page

#### Paragraphs within the body

1. Paragraphs are your regular text
2. The tag for a paragraph is `<p>`
3. Unlike headings, they **aren't** numbered

#### What every webpage is going to look like

    <!DOCTYPE html>
    <html>
        <head>
            <title>page title</title>
        </head>
        <body>
            content goes here
        </body>
    </html>

#### Recap

1. Remember to always close a heading or paragraph before starting another one
2. `<h1>` to `<h6>` only, there is no `<h7>` and beyond
3. There is only `<p>`

## Strong and emphasis

### The `<strong>`

1. Text inside `<strong>` indicates that it is of strong importance
2. Browsers make this text bold, but it also see the text as more important than the rest

### The `<em>`

1. The text inside `<em></em>` has stress emphasis.
2. Browsers make this text italic

### More about `<strong>` and `<em>`

1. They are both inline elements
    1. Use `<strong>` and `<em>` within a paragraph
    2. You must close a `<strong>` or `<em>` before the end of your paragraph
        1. Ex. `<p><strong>Warning:</strong> it's very cold out</p>`
    
#### Recap

1. Remember to always close a heading or paragraph before starting another one
2. `<strong>` is used for text that is of strong importance and is **bold** by default
3. `<em>` is to add emphasis and is *italic* by default

### File Naming and Organization

#### File Naming

1. Keep file names short
2. They should be descriptive (ex. "page2.html" vs. "about-us.html")
3. No spaces, use underscores or hyphens instead if you need space
4. Use lower case letters("About-Us.html" vs. "about-us.html" are two seperate files, the browser sees them differentlu)

#### File Organization
1. The main folder is called our **root folder** (The file that you're saving all of your stuff in)
2. The homepage **must be** index.html
3. The file, **index.html**, **must be in the root folder**, and not a sub-folder
    1. It won't work in the sub-folder
4. Other pages can be in sub-folders, depending on how you want to stay organized
5. Images should be placed in a sub-folder for better organization

