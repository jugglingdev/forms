# Interneting Is Hard - Forms

This is a solution to the [Forms tutorial No. 13 of HTML & CSS Is Hard](https://www.internetingishard.com/html-and-css/forms/).

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### Screenshot

![Forms screenshot](./forms.png)

### Links

- Solution URL: [Forms solution](https://github.com/jugglingdev/forms)
- Live Site URL: [Forms live site](https://jugglingdev.github.io/forms/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties

### What I learned

I really enjoyed this tutorial.  Supposedly forms are hard, but at least I find them fun to build.

The `<form>` element takes `action` and `method` attributes which define the web server's URL to process the data in the backend and how the form is submitted.  Use `method="post"` when changing data and `method="get"` when only getting data.

When making a text input field, use `<label>` and `<input>`.  The label's `for` attribute must match its input's `id` attribute likeso:

```html
<label for="full-name">Name</label>
<input id="full-name" name="full-name" type="text">
```

A new type of CSS selector from this tutorial is the attribute selector.  The following code will only select `<input>` elements with `type="text"`:

```css
.form-row input[type="text"] {
  background-color: #FFFFFF;
}
```

The `placeholder` attribute is also handy.  That's the one where you can display sample text in an input field for some nifty UX.

Another input type is `email` which the browser will validate either when clicking out of the field (Firefox) or when submitted (Chrome and Safari).

Speaking of validation, `:invalid` and `:valid` pseudo-classes are also useful for styling unacceptable and acceptable values.  Similarly, a `:focus` pseudo-class will style an element that the user is currently working on.

The next input type covered in this tutorial was `radio`.  For radio buttons, a `<fieldset>` wraps the radio button group and is labeled with a `<legend>`.  Then, each button is the `<input type="radio">` and its `<label>` is the text next to the button.  Here, it's important to use the same `name` attribute for each button in the group and different `value` attributes.  Using a `checked` attribute will select a button by default.

Since `<fieldsest>` does not support flexbox (at the time of this tutorial), floats was used.

Next up is dropdown menus.  Instead of using `<input>` plus `type`, they are coded with `<select>` plus an `id` and `name`.  They also have a matching `<label>` with a `for` element.  The difference here is that the dropdown has `<option>` elements as children, each with a unique `value` like in the T-Shirt Size dropdown from this tutorial.


After dropdowns comes textareas, which are pretty straightforward.  The main thing to note with them is that `<textarea>` needs a closing tag.  Any default text that will go in the text box is put between the `<textarea>` tags.

Coming up second-to-last is checkboxes.  Though checkboxes are similar to radio buttons, they do not require a `<fieldset>`.  In this tutorial, I wrapped the `<input>` element for the checkbox and the `<span>` element for the text in `<label>` tags to make it easier to match the final layout.

Finally, there's the submit button.  It uses a `<button>` tag and is pretty neat because it validates the `<input>` elements and submit it to the `action` URL where the backend server would take it from here.

### Continued development

The `<input>` element can also take attributes such as `required`, `minlength`, `maxlength`, and `pattern`.  I see some nice overlap with cybersecurity here in terms of validating identity and creating passwords.  These would be good to practice down the road.

Another topic I'm curious about is custom radio button CSS.  I remember learning about custom list item types, so I'm curious how similar they are to each other.

When working with dropdowns, the tutorial mentioned the challenges regarding styling dropdowns.  It's recommended to use Bootstrap Dropdowns or jQuery Selectmenus, both of which I'd like to look into for future projects.

Probably the biggest area for development regarding forms is in at submission.  There's a lot more going on in the backend that I'd like to explore such as using `action` to send the data to a backend URL and using AJAX queries to submit the form while staying on the same page.

### Useful resources

- [MDN Input](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input) - This covers the different input types and attributes.
- [MDN Advanced Form Styling](https://developer.mozilla.org/en-US/docs/Learn/Forms/Advanced_form_styling#Dealing_with_the_select_nightmare) - CSS styling for difficult elements such as dropdown menus.
- [JavaScript Bootstrap](https://getbootstrap.com/docs/3.4/javascript/) - Recommended for styling dropdown menus.
- [jQuery Selectmenu](https://jqueryui.com/selectmenu/#default) - Another option for styling dropdown menus.

## Author

- GitHub - [@jugglingdev](https://github.com/jugglingdev)

- freeCodeCamp - [@jugglingdev](https://www.freecodecamp.org/jugglingdev)

- Frontend Mentor - [@jugglingdev](https://www.frontendmentor.io/profile/jugglingdev)

- LinkedIn - [Kayla Paden](https://www.linkedin.com/in/kayla-marie-paden)

## Acknowledgments

Shoutout to Oliver James for his dedication to publishing and maintaining InternetingIsHard.com.  His tutorials were the first that really clicked for me.