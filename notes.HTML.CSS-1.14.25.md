# Notes for January 14-15, 2025

## Time Tracking

- 10 days left till deadline

### Github

1. GitHub is like Dropbox for code - it allows you store your code in the cloud so that you never lose it, even if the computer where you are writing it is lost

#### Repository

1. A **Repository** is Git's term for "a folder containing code"
2. You can also say "repo", for short

#### GitHub Codespaces

1. One of the most painful parts of learning how to program was just setting up your computer to be able to write and run code. We needed to install:
    1. An application to write our code with, known as a "**text editor**"
    2. The program that runs he code, known as the "**interpreter**". Each programming language has its own interpreter that reads files written in that language, executes the instructions contained within, and outputs the results. And each language has multiple versions, each of which has its own interpreter
    3. For most applications, we need to multiple languages installed
    4. A database (for our apps, we'll use a database called PostgreSQL)
    5. Many other utilities
2. We can avoid all this headache by writing and running our code on a *cloud* computer
    1. "**Cloud**" means that it's a computer sitting in someone else's warehouse somewhere, and we rent it from them
    2. It already has all of the software that we need installed on it, and we access it through our browsers
3. Since most developers *store* their code on GitHub.com nowadays, GitHub realized that it would be convenient to *edit* and *run* code there too
    1. GitHub recently released a product called **Codespaces**, which is a cloud **IDE** (integrated development environment) built right in to our repositories
    2. **Codespaces** is still in beta, but it's already quite polished and powerful

#### Codespace (VSCode) layout

1. A **Codespace** is primarily two things:
    1. A computer with exactly the software we need installed on it (Examples include Ruby, PostgreSQL, etc.)
    2. A program to write our code with, called a **text editor**. (Examples include vim, emacs, Sublime, Atom, Jetbrains, etc.)
        - The most popular one these days is VSCode, made by Microsoft. It's also the text editor Codespaces comes with.
2. To toggle the left pane (the file explorer and source control) in the VSCode environment, use the shortcut cmd + b
3. To toggle the bottom pane (the terminal and ports) in the VSCode environment, use the short cmd + j

#### Launching your app with `bin/server`

1. In the bottom pane or terminal window, the `%` is called the **bash prompt**
    1. Next to the bash prompt (`%`) is where you type in the command `bin/server`
2. The URL in the broswer tab where you have the live app preview running is the **host** of your app
    1. Example: `https://USERNAME-CODESPACE-NAME-vrpqrxxrx7x2rxx-3000.preview.app.github.dev`
3. To add a **path** that identifies which resource within the app we want to visit, type in a forward slash and then whatver HTML page you want to go to
    1. Example: `https://USERNAME-CODESPACE-NAME-vrpqrxxrx7x2rxx-3000.preview.app.github.dev/[THE FILENAME]`

#### `index.html`

1. `index.html` is the homepage of any site
2. You can get to it by using the previous method or by going to the **root path**, in other words, removing the `index.html` part after the `/` to visit the **bare domain**
3. It's the first page visitors see when they visit our domain

#### Git commit and sync

1. GitHub's core functionality is to allow us to save our code in the cloud. To do this, we need two things:
    1. Make a **git commit**, which is a snapshot of our entire project at a given moment in time
    2. **Sync** the commit from our codespace to `github.com/your-username/project-name`
3. Click on the **Source Control** button, enter a **commit message**, click the **Commit** button, and when you're ready to send your changes to your repository on GitHub.com, click the **Sync** button
4. If you don't **push** your commits from your codespace to your repository,  you might lose your work, because codespaces are automatically deleted after a period of inactivity. Pushing your commits to your repo will save your code forever. **ABC**! **A**lways **B**e **C**ommitting!

#### Open up the source code

1. You can open up the source code for any webpage with the keyboard shortcut, `cmd + option + U`, or `ctrl + U` in Windows

#### Link-in-bio notes

1. `<meta charset="UTF-8">` is a `<meta>` tag that greatly expands which characters we can use in our HTML document
    1. The default encoding (for historical reasons) is **ASCII**, which allows for just 128 english characters
    2. The **UTF-8 encoding** allows for over a million characters, including other language's alphabets, emoji, and more
    3. It's not *required*, but it is smart to add `<meta charset="UTF-8">` to every one of your HTML documents
    4. Add the `<meta>` element to the `<head>` of your HTML document
2. It's wise to create the bsaic structure of a page before cluttering it up with content
3. The following CSS: `<style> * { border: 1px red dashed; } </style>`, helps make it easier to build layouts
    1. The `*` selector targets *every* element in the document
    2. So, this style rule will add a red dashed border to every element
    3. After you get the layout the way you want it, you can delete or comment out this rule.
4. Since I want my links to open to a new tab when they're clicked, I need to include the `target="_blank"` attribute on them
5. When referencing the URL of one of my images in a `src="..."` attribute, start with a leading slash, `/`. This indicates the top-level, or "root", folder of the project workspace, so it's not in any subfolder
6. The **W3C HTML validator** analyzes yout code and points out any mistakes that it can find. Here is the link:
    1. https://validator.w3.org/#validate_by_input
7. Use the `object-fit: cover;` declaration or the `object-fit:` property to fix images that look squished when you forced their shape into a square
8. Use the `border-radius:` property to make an image circular
9. The `<html>` and `<body>` elements are, by default, only as tall as their content, so you'll notice the color gradiet repeating itself since the browser window (also known as the **viewport**) is taller than the content of the page and it doesn't look good
    1. To make the body fill the entire height of the window regardless of how tall the content is, use the `min-height: 100%;` declaration on both the `<html>` element and `<body>` element in your `<style>` element
10. Use `max-width:` instead of `width:` because it will make your webpage more responsive when your viewport is less than 640px. So, it will adapt and won't go past 640px when the viewport is wider than 640px.
    1. Writing CSS in this flexible way, to support users on a variety of devices, is called **responsive design**
    2. To get this to work right on phones, we need to add the following `<meta>` tag in the `<head>` of the document: `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
        - This `<meta>` tag will be included in every page and the values won't change
        - This `<meta>` tag tells phones to report their true viewport size to us, so that our CSS can respond accordingly
11. You can make an element grow to occupy all of the avaialble space in its parent with the `flex-grow:` property
12. You can remove underlines from links using the declaration, `text-decoration: none;`

#### Toggle font

1. With the `font-family:` property, you can change the font of your text
2. With the `font-weight:` property, you can make your text bolder
3. With the `font-size:` property
4. **Web Fonts** are font files we can deliver to a user like the way we deliver images, so we're not restricted to only using the fonts installed on the user's computer
5. There is a a very special web font called **Font Awesome**, where each "letter" in the font is a commonly used icon

#### Deploy websites using Render

1. Render can be used for the **static** websites, like the one we built, and also **dynamic** websites like the ones we'll eventually build with the Rails framework
2. Because we set render to deploy from our `main` branch on GitHub and connected the site with the GitHub repository, anytime you make a change to your site in a codespace and commit and push (sync) that change to publish it in the repository, the live app will automatically re-deploy with your updates

#### Using a custom domain name

1. A **TLD** is a **top-level domain**
    1. Examples include `.com`, `.dev`, `.inc`, etc.
    2. The cost of each varies
2. Domains ending in `.com` carry the most credibility, but they're the oldest and most desired, and therefore it's really hard to find a name that you want that's still available
3. `.dev` is a newer TLD that is commonly used by developers for their personal websites