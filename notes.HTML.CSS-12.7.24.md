# Notes for December 7, 2024

## Time Tracking

- 8:00 PM to 11:00 PM: Continue HTML and CSS crash course on Scrimba

## HTML and CSS

### Internal CSS

1. In general, inline CSS is never really used
2. We can use a **stylesheet**, rather than inline styles, to make more global changes
3. **We can use an internal style sheet that is placed in the head of our pages**
4. Every page can have a `<style>` element in the `<head>` element, which is where all the behind the scenes data goes

#### Example code for internal style sheet

    <head>
        <style>
            CSS goes here
        </style>
    </head>

### Selector

1. To choose what you want to style down below, use selectors, which is what we are selecting
2. To select the whole body of your page:
    - Ex.    **body** {
3. Selectors are followed by an opening curly brace
4. A **declaration** in CSS refers to the **property: value;** pair

### Rule

1. Made up of a **selector** and **property; value;** declarations
2. The selector, all the way down to the closing curly brace is what a rule is
3. When you declare a second property inside a rule, it's common practice to come down on another line like in the example below

#### Example of a rule

    p {
        color: #323232;
        font-size: 24px;
    }

### Selecting elements

1. Write the element, but without the opening and closing triangle brace (< >)
2. Do NOT include attributes
    - Ex. a {...}, p {...}, h2 {...}

### External CSS

1. With an external CSS file, we can have one stylesheet controlling *all* of our pages at the same time 
2. Be very careful using external CSS because one file controls **ALL** the styles, not the page you are on. If you change something from the stylesheet, or change something, ***it is changing for all the pages.***
3. Organization is key, so make sure to create a CSS file
    1. Keep files names generic like **style.css**
4. To change the background of all your pages, you'll have to select `body`
5. Bonus note: If you ever put only three numbers in a hex code, instead of 6, that's equivalent to writing the whole thing out.
    - Ex. background-color: #333; is  background-color: #333333;
    - Ex. background-color: #123; is background-color: #112233;
    1. So it's doubling them up

#### How do we connect our CSS files to our pages?

1. Instead of a style element, where we can write the, we can use **link**, which links to our CSS file
2. In the head of our document, we add: `<link href="css/style.css" rel="stylesheet">`
3. The `<a>` tag links to different documents and when you click on it, it takes you somewhere else, but the `<link>` tag links documents together
4. The `<link>` tag must always contain the **href** attribute and the **rel** attribute
5. The **rel** is the relationship, so what is the relationship of this file to the current page

## The relationship between HTML & CSS

### Three primary ways to select something

1. Element selector (which we've gone over)
    1. Simply write the element's tag, without the triangle brackets< >
    2. Do **not** include attributes
2. Class selector
    1. **Classes** are a type of attribute we can add to an HTML element
    - Ex. `<p class="intro">...</p>`
    2. In CSS, the class attribute is referenced by using a full stop (.)
    3. If you do `.intro`, it's going to select any paragraph with the class intro attribute on it
    4. The period (.) literally means class
    5. You can include the element before the classname, but you don't have to, nor is it recommended 
    - Ex. `p.intro {...`
##### Example of class selector

    .intro{
        font-size: 18px;
        color: #2b5dad;
    }

3. ID selector
    1. IDs are a type of attribute we can add to an HTML element
    - Ex. `<p id="intro">...</p>`
    2. An ID is represented by a hashtag instead of a dot

### ID vs Class

1. An ID is an individual
    1. An ID can only be used one time per page
    2. For example if you have `#main`, you can only have that `#main` on one element in that page
2. A class is a group
    1. A class can be used over and over again
    2. Classes can be used only once if you want
        1. If you use an ID and later on you realize you want to use it again, you'll have to go back and change it into a class, so just use classes
3. An ID will overwrite a class if they are both selecting the same thing

### Naming Classes and IDs

1. Spaces cause problems
    - Ex. `<div class="a box">` =/= (does not equal to) `.a box {...}`
    - Ex. `<div class="a-box">` == (equals to) `.a-box {...}`
2. Most CSS naming conventions will use a hyphenation (-), but some will use camel case (`.aBox`) or underscores (_)
3. You can include numbers in class and ID names, but the number can't be the first character



    

