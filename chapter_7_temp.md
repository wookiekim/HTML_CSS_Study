# Chapter 7 : Forms

Three different types of lists in HTML:
1. How to create a form on your website
2. The different tools for collecting data
3. New HTML5 form controls

The google searchbox in the middle of the page is also a form.

Form controls include:
* Adding text
  * Text Input, Password Input, Text Area
* Making choices
  * Radio buttons, Checkboxes, Drop-down boxes
* Submitting forms
* Uploading files

```
How forms work

1. The user fills in a form and submits to server
2. Name of each form control is sent to server along with user entry
3. Server processes information using languages such as PHP, C#, Java...
   > Or may store in a database
4. Server creates a new page to send back to the browser based on the information received.
```

Information is sent from browser to server in name/value pairs:
* ex) username=Ivy
* The name of form control should never be changed unless the code on the server can understand the changed name

### Form Structure
Form elements live inside the `<form>` element.
* requires `action` attribute
  * holds the URL for the page on the server that will receive the information in the form when submitted
* Also requires `method` attribute
  * forms can be sent using one of `get` of `post` methods
  * `GET`: values from the form are added to end of the URL specified in the action attribute
    * ideal for short forms, or when just retrieving information from the web server (not to be added/deleted to/from databse)
  * `POST`: values are sent in HTTP headers
    * allows user to upload a file
    * very long
    * contains sensitive data(ex passwords)
    * adds information to, or deletes information from a datbase
  * If not used, `get` method is used by default
* May use `id` attribute to identify the form distinctively from other elements on the page

`<input>` element used to create several different form controls.
* empty element, should end with `' /'`
* `type` atrtribute determines what type of input will be created
  * "text" for single-line text input
  * "password" for single-line, blocked out text input (asterisks, like `******`)
    * DOES NOT MEAN data in password control is sent safely to the server.
    * SSL (Secure Sockets Layer) should be used to ensure safety.
  * "radio" for radio buttons
    * allows to pick one of several options
    * `name` attr should be the same for all radio buttons for particular question
    * `value` specifies the value sent to server if selected
    * `checked` attribute used to indicate which value should be selected when the page loads (default check)
    * Radio button cannot be deselected. (need to select any 1)
      * Use checkbox instead for deselect
  * `type="file"` for file uploading
    * creates a [Browse] file to choose the file from.
    * the `<form>` element must have the `method` value set at 'post'.
  * `type="submit"` to act as a button to send a form over the server
    * does not need `name` attribute, but can be used
    * `value` specifies the words that appear on the button.
    * Appearance of the button can be customized using CSS.
  * `type="image"` for an image to be used as the submit button
    * need to include the `src` predicate
    * `alt, width and height` can be used as in an `<image>` tag.
  * "checkbox" allow users to choose one or more options to a question
    * `name` attr should be the same for all buttons for a particular question
    * `value` specifies the value sent to server if selected
    * `checked` attribute used to indicate which value should be selected when the page loads (default check)
  * `type="hidden"` to now show on page. 
    * Allows authors to add values to forms that users cannot see
    * ex) Which page the user was on when they submitted the form..

* `name` attribute to identify the form control
  * ex) to identify which is the password, which is the ID..
* `maxlength` attribute to limit the number of characters 
  * ex) year : maxlength of 4
* `size` attribute 
  * should not be used on new forms
  * used to indicate width of text input (measured by number of characters that would be seen)
  * now can be done through **CSS**

`<textarea>` element used to create multi-line text-input.
* Not an empty element (unlike other input elements), should have an opening and closing tag
* Default statement goes between the tags (ex `Enter your comments..`)
  * If not erased, sent to the server along with the user input
  * Javascript may be used to clear the default statement when clicked
* (old)`cols` attribute indicates how wide the text area should be (in number of character)
* (old)`rows` attribute indicates how many rows the text area should take up.
* Nowadays the width and height are controlled by **CSS**

`<select>` element is used to create a dropdown list box OR multiple select box
* Also requires `name`
* `<option>` element used for each options in the drop down menu
  * requires `value`
* `selected` attribute can be used to indicate the option that is selected on default.
* radio buttons are better if all the options should be visible at a glance
* If there are many choices, then dropdown list is better
* `multiple` attribute can be used to allow users to select multiple options from dropdown list
  * `multiple="multiple"`

Therefore Looks somewhat like:
```html

<html>
  <head>
    <title>Multiple Select Box</title>
  </head>
  <body>
    <form action="http://www.example.com/profile.php">
      <p>Do you play any of the following instruments? (You can select more than one option by holding down control on a PC or command key on a Mac while selecting different options.)</p>
      <select name="instruments" size="3" multiple="multiple">
        <option value="guitar" selected="selected">Guitar</option>
        <option value="drums">Drums</option>
        <option value="keyboard" selected="selected">Keyboard</option>
        <option value="bass">Bass</option>
      </select>
    </form>
  </body>
</html>
```

`<button>` element to allow other elements to appear inside the button
* and to have more control over how their buttons appear.
* can combine text and images between the opening `<button>` and closing `</button>` tag.


### Summary
* Whenever you want to collect information from visitors you will need a form, which lives inside a `<form>` element.
* Information from a form is sent in name/value pairs.
* Each form control is given a name, and the text the user types in or the values of the options they select are sent to the server.
* HTML5 introduces new form elements which make it easier for visitors to fill in forms.


