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

## Let's get to know each other!(10m)
- Introduce yourself!
  1. Name
  2. Where you're from
  3. What you do
  4. Which superhero would you be and why

## Opening Framing(5m)
- What brings you all here today? What are some things you all would like to accomplish?
- Creating things is something we can all get on board with, and we'll do just that, today!

## Hyper Text Markup Language(45m)
Show the google site. There's lots going on here. We're not going to be making this site or anything, but I want you get an idea that end of the day, it's just content.
- Show elements in dev tools for ebay
- Let's make some HTML!
- for windows users, you can use notepad, for mac users you can use text edit
- lets see if we can create a rudimentary website!
  - open up textedit/notepad
- as we go, put different elements we'll be using throughout the class
```html
<!DOCTYPE html>
<html>
  <head>
    <title></title>
    <!-- links to style sheets and scripts goes here-->
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <h1>hello world</h1>
    <p>some content</p>
  </body>
</html>
```

Open in browser, congratulations! We've made our first site!

Let's change up some of the content and shove the existing elements into a header tag If you guys are coding along, you can use this opportunity to make page about yourself! I'll be creating a page about this course, but the content, itself, is irrelevant, put whatever you want in there!:

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
the `<header>` tag is just used to separate out html code and give it semantic meaning

- create a `<section></section>` and nest
  - an `<h2></h2>` with some secondary header
  - a `<p></p>` and some content
  - and an `<img src=''>` with some internet picture

- create a `<footer></footer>` and nest
  - an `<a></a>`

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
    <section>
      <h2>HTML introduction!</h2>
      <p>HTML is a markup language that allows a coder to create content for a website</p>
      <img src='http://www.ilmuwebsite.com/wp-content/uploads/2014/05/html.jpg'>

    </section>
    <footer>
      <a href='https://www.facebook.com/mdndev'>Contact MDN on facebook!</a>
    </footer>
  </body>
</html>
```
### BREAK (5m)

## Cascading Style Sheets
- CSS is how your page will look. There's so much to learn about CSS. If you're interested, there are many different resources out there!
- Here's the thing about CSS, it's hard. Even once you think you're good at it, it has a way of frustrating you to no end.
- the basic idea of CSS is to select some HTML element and then do something to it.

First thing to do, is be able to link your style sheet to your web page.
- Create a css file in the same directory as your `index.html`
- then add `<link rel="stylesheet" href="styles.css">` in the `<head></head>` tags
  - lets test to see if it linked correctly

```
body{
  background: blue;
}
```

whoa! cool, too blue though
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
