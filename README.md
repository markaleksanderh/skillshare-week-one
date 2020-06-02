# Week One

## Goals

1. Install Homebrew, Git and VSCode (we'll only be using the last of these for this tutorial).
2. Become familiar with using the Terminal to create files and navigate through directories.
3. Become familiar with the basics of HTML and CSS by creating a static blog style webpage.

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


## Task

We're going to setup a static web page that displays the first few paragraphs of Franz Kafka's Metamorphosis. We'll add a few paragraphs and images.

The idea here is to get familiar with the structure of HTML and CSS.

### Terminal

Open VSCode from your applications folder. Go to _Terminal_ and click _New Terminal_.

Though it can be a little intimidating at first, using Terminal will massively speed up your development and you'll 

The following commands will come in handy:

| Command | Meaning |
| ------- | ------- |
| `pwd`   | Print working directory, i.e. prints the name of the directory you're in. |
| `ls`    | Returns a list of directories and files in the current directory |
| `cd`    | Change directory. Type `cd` followed by a space and the directory you want to move into, e.g. `cd app` |
| `mkdir` | Make directory. Type `mkdir` followed by a space and the name of the directory you want to make. e.g. `mkdir workspace` |
| `touch` | Creates a file. Type `touch` followed by the name of the file you want to create. Be sure to include the filetype e.g. `index.html` rather than `index`. |
| `rm` | Deletes a file. Type `rm` followed by space and the file you want to delete, e.g. `rm index.html`.
| `rmdir` | Deletes a directory. Type `rmdir` followed by space and the directory you want to delete, .e.g `rmdir styles` |


To find out which directory you're in, type `pwd` (for _print working directory_).

Before we get started, create a directory on your computer where you want to store all your work (something like "workspace" should suffice).

---

## Let's begin!

Open up Terminal in VSCode and type `pwd`. You should be in `/Users/<username>`. 
Enter `mkdir <directory name>` to create a new directory, e.g. `mkdir skillshare`.
Move to the directory you've just created by typing `cd <directory name>`, e.g. `cd skillshare`.

First, you'll want to our index HTML page, so go ahead and type `touch index.html`.



You have one of two options for viewing your HTML page in Chrome (or any other browser).
1. Open your browser and go to File > Open file. Navigate to the HTML file you want to view and open.
2. Setup a local server (Recommended). Your Mac should have both PHP and Python 2.x installed. For PHP enter `php -S localhost:8000`. For Python enter `python -m SimpleHTTPServer 8000`. Both will start a HTTP server on port 8000. Once your done, open up a browser tab and enter `localhost:8000` into the search bar.

Let's make a basic _Hello, World!_ page to make sure everything is working correctly.

In your `index.html` page, enter the following code:

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



## HTML

...

## CSS

...

### Working with Webfonts


### Working with Frameworks



---

## Stretch goal

1. Create a design for a page in Figma and try to recreate it in HTML and CSS.
2. Check your design across different browsers. Does the design look the same across all browsers? If not, how might you fix it?