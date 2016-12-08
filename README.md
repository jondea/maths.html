# Basic HTML: Personal website

As a student at Manchester you have two websites.

### Maths page
http://www.maths.manchester.ac.uk/~username

First ssh into your vummath account
```bash
ssh username@vummath.maths.manchester.ac.uk
```

Note: your landing page must be called `index.html`.

### Personal pages
http://personalpages.manchester.ac.uk/postgrad/firstname.lastname
Access your P drive (via my manchester) then place webpages into public_html

See http://personalpages.manchester.ac.uk/personalwebpages.html for more information

Note: your landing page must be called `default.htm`.

## Basic html

Make a file called `index.html`
```html
<!doctype html>
<html lang="en">
<head>
  <title>Title appears at top in browser</title>
</head>
<body>
  <div class="container">
    <h1>Heading</h1>
    <p>This is a paragraph</p>
    <img id="profile" src="image.jpg">
  </div>
</body>
</html>
```

And you're done!
The html is just a plain content, think of it as a series of boxes inside boxes.
There is some default styling (although it varies with browser) like content within h1 tags will be bigger, and after content inside p tags there will be a line break.

The tags should tell the browser what **kind** of content it is, this is called semantics. For example, a `<h1>` tag means the most important header, and `<p>` means paragraph. `<div>` means divider, and is the most generic tag, use it when there is no obvious name for the box.

### Links
Lets make another file called `publications.html` that looks like this
```html
<!doctype html>
<html lang="en">
<head>
  <title>My publications</title>
</head>
<body>
  <div class="container">
    <h1>Publications</h1>
    <p>I have not done anything of note for humanity yet.</p>
    <ul>
      <li>Things</li>
      <li>Other things</li>
    </ul>
  </div>
</body>
</html>
```
We can link to this using an anchor tag, add

```html
<a href="publications.html">My publications</a>
```
to `index.html`.
If you visit that page now, you should be able to click the link.
You refer to pages using the linux file notation.

## Styling using CSS

To style the content, we use a description language called CSS
To add a *stylesheet*, create a file called `style.css` and include it in the html file by adding the line

```html
<link rel="stylesheet" href="style.css">
```

inside the `head` tag.
The stylesheet will look something like this

```css
body{
  font-family: 'Open Sans', sans-serif;
}

.container{
  width:900px;
  margin:0px auto;
}

#profile{
  height:100px;
  width:50px;
}
```

It is a list of `selectors` like `body`,`.container` and `#profile` and attributes, like `width: 900px;`.
A dot on the selector means it is a class, a hash means id and no symbol means a tag type (like `body` or `p`).
Note that there should only be one element with a specific id but there can be any number of elements with a specific class.

Selectors can be combined and chained in various ways, for example

```css
.container h1{}
```

refers to a h1 tag inside a class called container.

```css
p, #profile{}
```

Refers to either a p tag or something with an id of profile.

## Useful tools

### Browser debuggers
You can access the developer tools on both firefox and chrome by pressing f12. The interface looks quite complicated but it allows you to inspect your (and other peoples!) site, and is a great tool for debugging problems. You can also use these tools to simulate your site on differently sized screens like mobiles or tablets.

## Frameworks
It is easy to make a quick website, but there are many subtleties to web design which are not obvious. Most pressingly, compatability. Screens come in a dizzying variety of physical size and number of pixels. It requires a great deal of knowledge and skill to produce a site from scratch which looks good on all screens.

Luckily, the work has already been done for you. There are many css frameworks which simplify the problem. First download the framework's css files then include them in your site's header (or just follow the instructions on the specific site). Then you can make use 

### Example frameworks

#### Bootstrap
http://getbootstrap.com/

Probably the most popular framework on the web, if you look very carefully, you can find this framework in use on the University of Manchester website.

It is full of features, but is also large. It is a little bit of overkill for a personal site.

#### Skeleton
A much simpler and much more efficient responsive framework. If you think bootstrap is overkill, try this framework.
http://getskeleton.com/

#### Pure
Very similar to above.
http://purecss.io/

### Using frameworks
As stated prviously, to use a framework, download it and include it on your site just like you would any other stylesheet. See the respective sites to see the components they include.

See `skeleton.html` for a basic example using the skeleton framework. Using the other two frameworks is very similar.

#### Container
The most basic component every framework has is the container. All of your content should go in here, and this just just handles the basic task of putting sensible amounts of padding and margin in. Even with just this, a basic text site should look good on all screen sizes (also known as responsive).

```html
<div class="container">
  <h1>Page title</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
</div>
```

#### Grids



## General strategy
Everything else, google it :)

The community of web developers is massive, almost every question you have has already been answered.