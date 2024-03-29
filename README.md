# Falix Help Center
![preview](https://i.imgur.com/PricFQB.png)

# Creating a New Article
Want to help contribute to the Help Center? Write or update an article!

## 🛡️ Requirements 
 - The communication must be clear and well explained for the user to understand
 - Fact check and make sure the information you're providing is accurate
 - Good grammar
 - Valid syntax
 - Proper metadata

## ✍️ Creating an Article
By following the file structure, create a `.md` file under the correct category. As an example, if you were to create an article that explains on how to install and use a plugin on Minecraft Java, the file would be created like `_posts_/minecraft/plugins/2021-08-04-plugin-name.md`. You're required to add the date at the beginning of the file name, `2021-08-04`. Then start writing the article in [Markdown](https://www.markdownguide.org/getting-started/). Writing in Markdown is very easy to do, if you need help understanding how to do certain task like creating a link, inserting an image, creating a list look [here](https://guides.github.com/features/mastering-markdown/).

## 📃️ Metadata
Make sure the metadata is setup properly, this is usually at the top of every article.
It should look like this:
```
---
layout: post
title:  "Title of Article"
categories: Minecraft
tags: plugins
permalink: /minecraft/plugins/name-of-plugin/
---
```

`layout` must remain as `post`.

`tags` is the sub-category.

## Content
### Plugin's Download
At the top of each plugin article, there is a box displays information about the plugin with a download link, example:

<img src="https://i.imgur.com/3tWsjYD.png">

If you plan to create an article explaining how to use a plugin, it's best you use this at the top of the article. The code is:
```
<div class="install-plugin">
    <img style="border-radius: 7px;" src="">
    <p>Name of Plugin</p>
    <a href="#">Download this Plugin</a>
</div>
```

In the future, I plan to add more content to this custom HTML code like author, official website, last updated, etc.

### Headers

# Header 1
```
# Header 1
```

## Header 2
```
## Header 2
```

### Header 3
```
### Header 3
```

#### Header 4
```
#### Header 4
```

### Links
[FalixNodes](https://falixnodes.net/)
```
[FalixNodes](https://falixnodes.net/)
```

### List and Check Lists
List:
 - Item
 - Item
 - Item
 - Item
```
 - Item
 - Item
 - Item
 - Item
```

Checklist:
 - [x] Item
 - [x] Item
 - [ ] Item
 - [ ] Item
 - [ ] Item
```
 - [x] Item
 - [x] Item
 - [ ] Item
 - [ ] Item
 - [ ] Item
```

### Tables
A table is used to display content clearly without making a mess, like we did in the [Getting Started](https://help.falixnodes.net/minecraft/general/getting-started/#message-of-the-day) article under Minecraft, showing a color code table.

Example: 

| Example        | List          |
|:---------------|:--------------|
| Example        | Content       |
| Example        | Content       |
| Example        | Content       |
| Example        | Content       |

Code:
```
| Example        | List          |
|:---------------|:--------------|
| Example        | Content       |
| Example        | Content       |
| Example        | Content       |
| Example        | Content       |
```

### Video
I personally like seeing `<video>` in the help center over a YouTube embed, but you're allowed to use a YouTube embed if you want to.
[Learn how to embed a YouTube video](https://support.google.com/youtube/answer/171780?hl=en)

We've added VideoJS script recently to the help center, which adds custom controls to the code.

So when adding videos to an article, make sure it looks like this:

```
<video class="video-js" controls preload="auto" data-setup="{}"><source
 src="https://example.com/video.webm" type="video/webm"
 src="https://example.com/video.mp4" type="video/mp4"
 /></video>
```

Make sure to provide both webm and mp4. Webm are much smaller and load faster, although an MP4 file is required as not all browsers support webm format. So the MP4 is more of a fallback option if the user's browser doesn't like the webm format.

## 📢️ Publishing
Create a pull request on this repo and title it like this "New Post: Name of Article" or if you're editing an article, title it like "Edit: Name of Existing Article".

Your edit will be reviewed by [Korbs](https://github.com/KorbsStudio/) along with your code to check for any syntax error.

# Building
If you're interested in learning on how to build the Help Center locally, maybe to preview that your article does show up properly, just follow the instructions below.

Since the Help Center is powered by Jekyll, you'll need to install [Ruby](https://www.ruby-lang.org/en/) for your operating system.
 - [Download for Windows](https://rubyinstaller.org/)
 - [Download for macOS](https://www.ruby-lang.org/en/downloads/)

### Installing Ruby on Linux
Debian/Ubuntu:
```
sudo apt-get install ruby-full build-essential zlib1g-dev
gem install jekyll bundler
bundle install
```
Fedora/RedHat:
```
sudo dnf install make automake gcc gcc-c++ kernel-devel ruby-devel
gem install jekyll bundler
bundle install
```

## Building and Locally Hosting

To run a localhost server, run:
```
bundle exec jekyll serve
```

After using `bundle exec jekyll serve`, try going to http://localhost:4000/ in your preferred web browser.
