# Intro to HTML/CSS

## LO's
- Differentiate between HTML and CSS
- Explain how HTML is used for content
  - Know which content goes in the head
  - know which content goes in the body
- Explain how CSS is used for styling
- Link a style sheet to HTML
- utilize common HTML tags/elements
- understand how selectors work in css
- utilize common css properties
- deploy static site using bitballoon

## Let's get to know each other!()
- Introduce yourself!
  1. Name
  2. Where you're from
  3. What you do
  4. Which superhero would you be and why

## Opening Framing()
HTML and CSS is at the crux of everything that we do as web developers. Whether it's leveraging HTML using advanced frontend frameworks/libraries or simple static content.

## Hyper Text Markup Language()
Let's first talk about Hyper Text Markup Language. HTML is a cornerstone technology, used by most websites to create visually engaging webpages, user interfaces for web applications, and user interfaces for many mobile applications. HTML establishes a structure for the website and marks up the content to provide semantic meaning.

Let's take a look at a popular [website](http://www.google.com). I'm sure most everyone's familiar with google, but I want to show you this web page in a different light.  I'm going to open the Developer tools, I do this by hitting `cmd` & `option` & `i`(`Ctrl` & `Shift` & `i`- for PC) on the keyboard.

The first thing I want to do, is just click on the tab that says `Elements` in the dev tools. When we click this, we see something that, to be honest, scares me. Oh em gee `class onload try{if(!google.k.b)} data catch new Image src`. What does it all mean?! Believe it or not, what you see is all of the HTML for this page of the web application. HTML can get pretty complex, but let's look at what it's doing at its core.

 In the top left of the dev tools(if you're using chrome), you'll see and icon that is a box with a mouse cursor in the middle of it. I'm going to use this tool to inspect some elements in the HTML. Specifically, I'm going to click on the webpage where it says `Images` in the top right.

```html
<a class="gb_P" href="https://www.google.com/imghp?hl=en&amp;tab=wi&amp;authuser=0&amp;ei=alyWVqL6OMjXeYflrKAL&amp;ved=0EKouCBQoAQ" data-pid="2">Images</a>
```

(ST - WG) What can you see is the same in the webpage as the code you see here.

`Images`!! At the end of the day, HTML is just content.

Let's make some HTML!
> for windows users, you can use notepad, for mac users you can use text edit. Alternatively, if you have Sublime, that would be best.

1. First thing you should do is create a folder on your desktop called `my_first_website`
2. Next open your text editor(sublime, notepad, textedit, etc..)
3. Create a new file and save the file as `index.html` in the `my_first_website` folder you created before.

> These lasts steps are pretty important to follow along with the class! So make sure you get with an instructor to be at the right place.

Before we start writing HTML. I want to give you a general overview of how we write it. Essentially it boils down to HTML elements that are called `tags` and contents that go inside of them. Sometimes it will be other tags, other times it will be text that wants to be displayed in your web page. We'll be going over only *some* of the tags today. I encourage you to investigate others and how they work.

> Also note, that I will be coding an "Intro to HTML and CSS" website, but you're free to make up your own content instead of using the content I'm providing! Maybe, a site about puppies, Starwars or pterodactyls with laser beams for eyes.

### The Head

Let's start writing some `html`. In the `index.html` file we've created:

```html
<!DOCTYPE html>
<html>
</html>
```

> `<!DOCTYPE html>` is a document type declaration for HTML 5. The `<html>` tags are the delimiters of our web pages content. Everything we write in HTML today will be inside of the `<html>` tags.

If we open this file in the browser. We see ... absolutely nothing.

Let's talk about the head.

```html
<!DOCTYPE html>
<html>
  <head>

  </head>
</html>
```

Again, nothing's changed. What kind of information do you think would go in the head? (ST-WG)

```html
<!DOCTYPE html>
<html>
  <head>
    <title>HTML intro!</title>
  </head>
</html>
```

If we look in our browser this time, something has changed! What is it?

> It's often a misconception from people that do not code to assume what goes in the head is the stuff at the top of a web page. In reality, the `head` tag contains meta data. Things like, stylesheets, scripts, character sets, language encoding and other sorts of things like that. The `title` element gives our page a title and can be important for SEO. Additionally, looks at the chrome tab in your browser window!

### Your first webpage

Finally let's add some actual content. This will go in the `body` tag.

> The `body` tag is where all of our webpages main displayed content will live.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>HTML intro!</title>
  </head>
  <body>
    <h1>Intro to HTML!</h1>
    <p>This is an awesome new site using html and css!</p>
  </body>
</html>
```

Open in browser, congratulations! We've made our first site with actual content!

> Here we're using an `h1` tag which is one of 6 heading tags(`h1` through `h6`). Add an `h2` to the document, what's different about the h2 and h1? One is bigger than the other. With regard to HTML the size difference has no bearing on the *semantic* difference. The idea is that `h1`s are more important headings than `h2`s. The size difference is coming from default CSS styles for those headers. Additionally, we're also using a `<p>` tag which semantically identifies the content within as a "paragraph"

### The Header

Let's change up some of the content and shove the existing elements into a `<header>` tag :

```html
<!DOCTYPE html>
<html>
  <head>
    <title></title>
    <!-- links to style sheets and scripts goes here-->
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <header>
      <h1>Intro to HTML!</h1>
      <p>This is an awesome new site using html and css!</p>
    </header>
  </body>
</html>
```
> the `<header>` tag is just used to separate out html code and give it semantic meaning for the elements nested within it.

### The main

Let's add some main content to our webpage. We'll be using the `<main>`.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>HTML Intro!</title>
  </head>
  <body>
    <header>
      <h1>Intro to HTML!</h1>
      <p>This is an awesome new site using html and css!</p>
    </header>
    <main>
      <h2>HTML introduction!</h2>
      <p>HTML is a markup language that allows a coder to create content for a website</p>
      <img src='http://www.ilmuwebsite.com/wp-content/uploads/2014/05/html.jpg'>
    </main>
  </body>
</html>
```

> The only new element we've added is the `img` tag. Couple of new things for this tag. We'll be using an attribute for the first time. There are alot of use cases for attributes in HTML elements, this is just one of them. The `src` attribute provides where the image is coming from. Another thing to note is that `<img>` is a self closing tag.

In order to create an image of a personal picture of yours. Place the picture that you'd like in your webpage in the *same* directory as that of you `index.html`(your webpage). Then link to it in the src with just the files name eg.:

```html
<img src="my_pic.jpg">
```

> Computers are VERY specific, so make sure you have capitalization correctly. Additionally it has trouble with white spaces, so you may want to rename the picture such that its all lower case with no spaces like in the example above.

### The Footer

Let's add some footer content to it. We'll be using the `<footer>` tag.

> the `<footer>` tag is just used to separate out html code and give it semantic meaning for the elements nested within it.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>HTML Intro!</title>
  </head>
  <body>
    <header>
      <h1>Intro to HTML!</h1>
      <p>This is an awesome new site using html and css!</p>
    </header>
    <main>
      <h2>HTML introduction!</h2>
      <p>HTML is a markup language that allows a coder to create content for a website</p>
      <img src='http://www.ilmuwebsite.com/wp-content/uploads/2014/05/html.jpg'>
    </main>
    <footer>
      <a href='https://www.facebook.com/mdndev'>Contact MDN on facebook!</a>
    </footer>
  </body>
</html>
```

> The anchor tag(`<a>`) is used to create links to other sites. It has an attribute `href`. Whatever is in quotes after the `href=` is the link that it will go to.

That's it for HTML!

> We've just barely scratching surfaces in this class. If you'd like more information about HTML check out these [docs](https://developer.mozilla.org/en-US/docs/Web/HTML)

## Cascading Style Sheets
Cascading Style Sheets (CSS) is a style sheet language used for describing the presentation of a document written in a markup language. There's so much to learn about CSS. If you're interested, there are many different resources out there!(check the bottom of the lesson plan for them!)

Here's the thing about CSS, it's hard. Even once you think you're good at it, it has a way of frustrating you to no end. You could take an entire 3 month course on CSS and still not know its full breadth.

The basic idea of CSS is to select some HTML element and then do something to it.

### First Steps
Create a new file and save the file as `styles.css` in the `my_first_website` folder you created before. We now need to link this stylesheet to our web application.

In the `<head></head>` tags of your `index.html` add a `link` element like this:

```html
<link rel="stylesheet" href="styles.css">
```

Let's see if it worked by adding this next bit of code to our `styles.css`

```css
body{
  background: blue;
}
```

whoa! cool!

Everything's super blue, but how? Lets breakdown what we just wrote.

The entirety of what we wrote is known as a CSS rule. It's comprised of a couple of component parts.

The first being, the selector. In this case, `body`. In a nutshell when we write:

```css
body{

}
```

We're telling the html/css that were about to do something to all `body` elements. Theres only one in this case, but if it were `p` it would apply to all paragraphs. What follows the selector are some `{}` that act as delimiters for the CSS code we'll be putting in to be applied to what's selected.

 too ugly.... though
[Color Picker](http://www.color-hex.com/)

- Use this link instead! to pick a color of your choosing
- Lets align some text
```
body{
  background: blue;
  text-align: center;
}
```

Hmm, I think I like the content being centered, but I think it'd be really nice if my header was aligned to the left. Let's do eet!

```
body{
  background:blue;
  text-align:center
}

header{
  text-align:left
}
```

Talk about "cascading", add another body selector, change the color and show which one shows up as the color

### Bitballoon
- sign up for an account
- drag and drop your folder and your site is hosted!

If time allows:
- border
- margin
- padding
- color
- font-family
- height
- width
- html classes/id's for selectors
- linking to another page in your directory



### Documentation
[HTML documentation](https://developer.mozilla.org/en-US/docs/Web/HTML)

[Getting Started with CSS](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started)

[CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)

[CSS tricks alamanac](https://css-tricks.com/almanac/)
