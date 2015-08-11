---
  layout: post
  title: Html Forms And Jquery
  language: jquery
---

Lots of the interaction on the web happens through forms. In general, when you type something into a text box, clicking a checkbox or radio button, or sliding a slider, you are interacting with an HTML Form.

Facebook status update? Form. Tweet? Form. Instagram picture upload? Form!

So, how do we get form data with jQuery?

As users are entering text in HTML text fields or changing values of checkboxes, sliders, and radio buttons, the browser is smart enough to already be updating the DOM with that information. Because the data is in the DOM, we can get it with javascript, and use it!

If we have an html input on our webpage:
```
Enter your text here:
<input type="text">
```

Then we can get it with jQuery:
```
var user_text = $('input').val();
```
And once we have it, we can use what we know to show it back to them:
```
$('# results').text(user_text);
```
Of course, we can manipulate the text before displaying it to the user.
```
var user_text = $('input').val();
$('# results').text(pigLatin(user_text));
```
HTML Forms have all kinds of input that we can play with.
```
<form>
  Name:
 <input type="text" value="name">
 How was your experience today?
 <select name="rating">
  <option value="strange">Strange</option>
  <option value="unnerving">Unnerving</option>
  <option value="spooky">Spooky</option>
  <option value="shocking">Shocking</option>
  <option value="blase">Blase</option>
</select>
 What was your favorite?
<input list="favorites">
<datalist id="favorites">
  <option value="ghost">
  <option value="clown">
  <option value="werewolf">
  <option value="vampire">
  <option value="wereclown">
</datalist>
 Feedback:
 <textarea name="feedback" rows="10" cols="40">
 <button onclick="showResults()">Show Results</button>
</form>
```
We see:
- text inputs
- select from options
- dropdown list
- textarea
- buttons

There are even more elements to find and use - try searching for them!
