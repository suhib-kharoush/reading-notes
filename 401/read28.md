# Django: Working with forms
- In this tutorial, we'll show you how to work with HTML Forms in Django, and, in particular, the easiest way to write forms to create, update, and delete model instances.

### Django form handling process:
- Django's form handling uses all of the same techniques that we learned about in previous tutorials (for displaying information about our models): the view gets a request, performs any actions required including reading data from the models, then generates and returns an HTML page (from a template, into which we pass a context containing the data to be displayed).

- A process flowchart of how Django handles form requests is shown below, starting with a request for a page containing a form (shown in green).
![](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms/form_handling_-_standard.png)
- Based on the diagram above, the main things that Django's form handling does are:
1. Display the default form the first time it is requested by the user.
- - The form may contain blank fields (e.g. if you're creating a new record), or it may be pre-populated with initial values (e.g. if you are changing a record, or have useful default initial values).
- - The form is referred to as unbound at this point, because it isn't associated with any user-entered data (though it may have initial values).

2. Receive data from a submit request and bind it to the form.
- - Binding data to the form means that the user-entered data and any errors are available when we need to redisplay the form.

3. Clean and validate the data.
- - Cleaning the data performs sanitization of the input (e.g. removing invalid characters that might be used to send malicious content to the server) and converts them into consistent Python types.
- - Validation checks that the values are appropriate for the field (e.g. are in the right date range, aren't too short or too long, etc.)

4. If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields.

5. If all data is valid, perform required actions (e.g. save the data, send an email, return the result of a search, upload a file, etc.)

6. Once all actions are complete, redirect the user to another page.

### Form:
- The Form class is the heart of Django's form handling system. It specifies the fields in the form, their layout, display widgets, labels, initial values, valid values, and (once validated) the error messages associated with invalid fields.

### Declaring a Form:
- The declaration syntax for a Form is very similar to that for declaring a Model, and shares the same field types (and some similar parameters).
