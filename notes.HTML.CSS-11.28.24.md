
# Notes for November 28, 2024

# Happy Thanksgiving!

## Time Tracking

- 1:15 PM - 3:15 PM: Begin HTML and CSS crash course on Scrimba

## The Building Blocks of the Web

- HTML
- CSS
- Javascript

### HTML

1. HTML stands for **H**yper**T**ext **M**arkup **L**anguage
    1. Hypertext means it has links in it
    2. Markup language: a language where you can write something that conveys meaning to the processor, to the browser, or to the computer.
2.  The content of websites
    1. All the content you see on a website comes from HTML
3. Straightforward and easy to learn

### CSS

1. CSS stands for **C**ascading **S**tyle **S**heets
2. Manages how our websites look
    1. Fonts, colors, backgrounds, layouts, and more

### Javascript

1. Programming language
    1. It's one of the programming languages that browsers can understand
2. Can manipulate HTML and CSS
3. Used for simple manipulations to create full web applications
4. Javascript makes a website more interactive

### HTML and CSS Continued

1. HTML is all you need to make a website
    1. If you only have HTML then you have a functioning webpage
    2. The only issue is that HTML looks incredibly boring
2. CSS makes the site look interesting
    1. It holds attention and keeps people around to check out the content of the page.
3. So, HTML = content and CSS = how the webpage looks (hooks)

## HTML - terminology & syntax

1. Tells the browser what the content we are writing actually is
    1. Whether it's a heading, paragraph, or anything else, the browser needs to be told what it is
    2. We can make a link, add bold or italic text
    3. We can tell the browser if it's the navigation section, the footer, or the main content of the page
2. We need to define all the content we're writing using HTML
3.  The basic syntax of HTML uses something called **Tags**

### Tags

1. When writing HTML we wrap everything in tags to tell the browser what is what
2. Every tag is wrapped up in triangle brackets (**< >**) and they tell the browser that this is a tag and not the actual content itself
3. Just like how books have a front and back cover, tags act as the cover for the content
    1. The **opening tag** (**< >**) works as the front cover and the **closing tag** (**</ >**) works as the back cover
4. When you have an opening and closing tag, all together, that gives you something called an **element**

#### Recap on tags

1. Tags are always inside of triangle brackets (**< >**)
2. Closing tags include a forward slash (**</ >**)
3. Everything from the opening and closing tag is called an element
4. Elements define our content to the browser

## Basic file structure of HTML

### `<!DOCTYPE html>`

1. The first thing you'll see at the top of every document is **`<!DOCTYPE html>`**
    1. It tells the browser that this is an HTML5 document

### `<html>`

1. Once we've told the browser that it's looking at an HTML5 document, we need to tell it that we're starting to write HTML by using the tag, **`<html>`**
    1. You can have CSS and Javascript inside an HTML document as well
    2. `<html>` acts as the "root" of our document because **everything** lives inside our `<html>` element

### The `<head>`

1. Nothing here is visible to the visitor
2. The `<head>` is the essential information
    1. The `<head>` has some meta tags that you can put in it like the author, a description of the site, and more
3. It's more of a "brain" than a "head" because a head you can see, but the brain is what you can't see that's controlling everything from the shadows...

### `<title>`

1. Inside the head of the document is where we have our `<title>`
2. Since it's in the `<head>`, it won't be visible, but it shows up in the tab of the browser and in search results

#### Write out the code for what you've learned so far

    <!DOCTYPE html>
    <html>
        <head>
            <title>Muscle Memory</title>
        </head>
    </html>

