# Week One

## Goals

1. Install Homebrew, Git and VSCode (we'll only be using the last of these for this tutorial).
2. Become familiar with using the Terminal to create files and navigate through directories.
3. Become familiar with the basics of HTML and CSS by creating a static blog style webpage.

There is quite a lot to cover here so if we spend two weeks going over it that's fine!

***

## Setup

This week we're going to begin learning the basics of HTML and CSS, but first we need to install three applications.

### Homebrew

First, let's install Homebrew. Homebrew is a package manager for macOS.

Open your terminal and paste in `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`.

### Git

Next, we need to setup your Git account. Go to `https://github.com/join` and setup an account.

Install Git through Homebrew and configure your credentials.

### VSCode

Next, we need to install a text editor. I recommend using VSCode, but you could also use Sublime Text or Atom if you prefer. I prefer VSCode because it has a terminal integrated into the application which is useful if you only have one display to work with (when it comes to working with shell or looking through server logs you'll want a second display just for the terminal).

To install VSCode, head to `https://code.visualstudio.com/docs/setup/mac`.


***

## Task

We're going to setup a static web page that displays the first few paragraphs of Franz Kafka's Metamorphosis. We'll add a few paragraphs and images. Feel free to choose your own sample text and images.

The idea here is to get familiar with the structure of HTML and CSS.

### Terminal

Open VSCode from your applications folder. Go to _Terminal_ and click _New Terminal_.

Though it may be a little intimidating at first, using Terminal will massively speed up your development and you'll become more comfortable with it the more time you spend using it.

The following commands will come in handy:

| Command | Meaning |
| ------- | ------- |
| `pwd`   | Print working directory, i.e. prints the name of the directory you're in. |
| `ls`    | Returns a list of directories and files in the current directory |
| `cd`    | Change directory. Type `cd` followed by a space and the directory you want to move into, e.g. `cd app` . Use `cd .. ` to navigate back to the immediately preceding directory. |
| `mkdir` | Make directory. Type `mkdir` followed by a space and the name of the directory you want to make. e.g. `mkdir workspace` |
| `touch` | Creates a file. Type `touch` followed by the name of the file you want to create. Be sure to include the filetype e.g. `index.html` rather than `index`. |
| `rm` | Deletes a file. Type `rm` followed by space and the file you want to delete, e.g. `rm index.html`.
| `rmdir` | Deletes a directory. Type `rmdir` followed by space and the directory you want to delete, .e.g `rmdir styles` |
| `pwd` | Print working directory. Prints the directory you're in. |


***


## Let's begin!

Select Terminal in the menu in VSCode and select New Terminal to open a new terminal window. If you type `pwd` you should be in `/Users/<username>`.

Enter `mkdir <directory name>` to create a new directory, e.g. `mkdir skillshare`.
Move to the directory you've just created by typing `cd <directory name>`, e.g. `cd skillshare`.

First, you'll want to create our index HTML page, so go ahead and type `touch index.html`.


### Viewing your document

You have one of two options for viewing your HTML page in Chrome (or any other browser).

1. Open your browser and go to File > Open file. Navigate to the HTML file you want to view and open.

2. Setup a local server **(Recommended)**. Your Mac should have both PHP and Python 2.x installed. For PHP enter `php -S localhost:8000`. For Python enter `python -m SimpleHTTPServer 8000`. Both will start a HTTP server on port 8000. Once your done, open up a browser tab and enter `localhost:8000` into the search bar. When you enter this command, the script will look for a file named either `index.html` or `index.htm` so make sure your HTML file is named correctly!

Let's make a basic _Hello, World!_ page to make sure everything is working correctly (FYI displaying _Hello, World!_ is usually the first thing you learn when learning _any_ new language).


Let's go back to our `index.html` page. Open it up in VSCode and enter the following code:


```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>Hello, World!</title>
    </head>
    <body>
        <h1>Hello, World!</h1>
    </body>
</html>
```

Refresh your browser. You should see the following in your browser:

![alt text](tutorial-images/helloworld.png)



Let's dissect the code above to understand what's going on.

### Document type

The first line `<!DOCTYPE html>` is called a document type declaration. It's unlikely we'll need to look at any other document type (e.g. XML) during this Skillshare, so it should be sufficient to just remember we need to include this as the first line of the HTML document.

The next line `<html lang="en">` is the root element of the document. The `lang="en"` attribute declares that the document is in English (important for accessibility).



### Head

Next, we see the `head` element. This element contains all the metadata related to a document (essentially data that isn't displayed when a user opens their browser).

#### Meta tags

There is a broad range of metadata we may need to add to the `head` element. Examples include:

- `charset` which tells the browser which character encoding the document uses. `utf-8` supports pretty much any language we'll need so it's unlikely we'll need to use another character set.

- Keywords metadata (how search engines would find your page ~20 years ago). `<meta name="keywords" content="Skillshare, Skill, Share, HTML, CSS">`. For various reasons (e.g. keyword stuffing), this is rarely used and not recommended.

- Images and description that's displayed when a user posts your site in a tweet on Twitter. `<meta name="twitter:card" content="summary"></meta>`

### Title

The head is also where we declare the document title. The document title will appear in the browser tab and if a user saves the webpage in their bookmarks.

It's also possible to set the document title dynamically but we'll cover that later.

### External files

The `head` element is also where we will link to our CSS document:

`<link rel="stylesheet" href="styles.css">`

The `rel` attribute denotes the relationship of the link to the document whereas `href` or _hypertext reference_ specifies the location of the resource (e.g. stylesheet, icon, document).

You'll use similar markup to declare your favicon:

`<link rel="shortcut icon" href="/favicon.ico">`

If we were including JavaScript, the `head` would also be where we would include a link to our scripts `<script src="index.js">`, but more of that later.



### Body


You may have noticed that each element in the code has both an opening `<>` tag and a closing `</>` tag. The tags appearing beneath (and helpfully indented by most text editors) are contained within the preceding element.

A word on terminology here:

- Tag: `<p>`
- Element: `<p></p>`

Some elements do not require closing tags and are called _empty elements_, e.g. a line break `<br>` or an image `<img>`.




Now that we've covered the basics, let's get on with building our first web page.

***

Add image of the site we want to create.

## HTML

...

## CSS

CSS stands for _cascading style sheets_. Meaning - 

CSS uses a different syntax from HTML.
Propety + syntax
Selector + declaration block



There are three ways of adding style to an element.

- Inline - style is added as an attribute to a tag, e.g. `<p style="color: red;>"`.
- Embedded - style is added between `style` tags in the header, e.g. `<style> p { color: red; }</style>`.
- External - styles added in a separate sheet and referred to using the `link` tag, e.g. `p { color: red; }`.

Generally speaking, you should never use inline styles because it's too difficult to maintain. I'd also recommending avoiding embedded styles unless you're working on a very small proof of concept and need to save time. You'll find it easier and cleaner to contain all your styles in a different sheet, so that's what we'll do here.




### IDs and Classes

In order to select a single element, use an ID. The ID is added to the individual HTML element you wish to select. As a rule, an ID should only be used once on the page.

ID is added as an attribute to the opening tag and selected from CSS:

#### HTML
```
<h1 id="page-title">
```
#### CSS
```
#page-title {
    margin: 5px;
}
```

Best practice dictates that we include the element type when selecting the element in CSS. This will make it easier to identify which element you're referring to when editing your CSS later.

```
h1#page-title{
    margin: 5px;
}
```

Alternatively, if you expect to use an element more than once on the same page, use a class.

#### HTML
```
<p class="body-text">
```

#### CSS
```
.body-text {
    font-size: 12px;
}
```

As with IDs, we can skip the element name but it's good practice to include it.

```
p.body-text {
    font-size: 12px;
}
```


### Working with Webfonts


Cover web safe fonts.
Google Fonts.


### Working with Frameworks

Bootstrap.
Ionic.

Positives, negatives.




---

## Stretch goal

1. Create a design for a page in Figma and try to recreate it in HTML and CSS.
2. Check your design across different browsers. Does the design look the same across all browsers? If not, how might you fix it?