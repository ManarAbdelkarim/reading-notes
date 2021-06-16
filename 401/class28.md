# Django CRUD and Forms
![](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms/admin_book_add.png)
## What is Forms:
- An HTML form is used to collect user input. The user input is most often sent to a server for processing.
- The <form> HTMAn HTML Form is a group of one or more fields/widgets on a web page, which can be used to 
collect information from users for submission to a server.L element represents a document section containing interactive controls for submitting information.
- The form is defined in HTML as a collection of elements inside <form>...</form> tags, containing at least one input element of type="submit".
  
## submit :
  The submit input will be displayed as a button (by default) that can be pressed by the user to upload the data in
  all the other input elements in the form to the server The form attributes define the
  HTTP method used to send the data and the destination of the data on the server
  
## (action):

- `action:` The resource/URL where data is to be sent for processing when the form is submitted. If this is not set (or set to an empty string), then the form will be submitted back to the current page URL.
- `method:` The HTTP method used to send the data: post or get.
- `The POST` method should always be used if the data is going to result in a change to the server's database because this can be made more resistant to cross-site forgery request attacks.
- `The GET` method should only be used for forms that don't change user data (e.g. a search form). It is recommended for when you want to be able to bookmark or share the URL
  

## creating a form using Django:

1. Declaring a Form:
  
      from django import forms

      class RenewBookForm(forms.Form):
        renewal_date = forms.DateField(help_text="Enter a date between now and 4 weeks (default 3).")
  
 2. Form fields
  
   BooleanField, CharField, ChoiceField, TypedChoiceField, DateField, DateTimeField, DecimalField,
   DurationField, EmailField, FileField, FilePathField, FloatField, ImageField, IntegerField, GenericIPAddressField,
   MultipleChoiceField, TypedMultipleChoiceField, NullBooleanField, RegexField, SlugField, TimeField, URLField,
   UUIDField, ComboField,
   MultiValueField, SplitDateTimeField, ModelMultipleChoiceField, ModelChoiceField.

  
  *The arguments that are common to most fields:*
  
- required: If True, the field may not be left blank or given a None value. Fields are required by default, so you would set required=False to allow blank values in the form.
- label: The label to use when rendering the field in HTML. If a label is not specified, Django will create one from the field name by capitalizing the first letter and replacing underscores with spaces (e.g. Renewal date).
- label_suffix: By default, a colon is displayed after the label (e.g. Renewal date:). This argument allows you to specify a different suffix containing other character(s).
- initial: The initial value for the field when the form is displayed.
- widget: The display widget to use.
- help_text (as seen in the example above): Additional text that can be displayed in forms to explain how to use the field.
- error_messages: A list of error messages for the field. You can override these with your own messages if needed.
- validators: A list of functions that will be called on the field when it is validated.
- localize: Enables the localization of form data input (see link for more information).
- disabled: The field is displayed but its value cannot be edited if this is True. The default is False.
