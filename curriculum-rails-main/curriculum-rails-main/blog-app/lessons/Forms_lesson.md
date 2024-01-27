# Forms

## Learning objectives

- Use preprocessed html file with embedded Ruby code.

### Estimated time: 1h

## Description
Forms in Rails are largely the same as standard forms in HTML, with the addition of some pretty great form helpers. Their use is the same though, so all there is to focus on is some new syntax. 

- **Be aware:** Rails protects itself from [CSRF](https://guides.rubyonrails.org/security.html#csrf-countermeasures) attacks so if you don't create your form using helpers, you may encounter some errors and will need to provide a `form_authenticity_token`. Don't worry about understanding CSRF at this time, just be aware that it is something to be accounted for.

### Why is understanding Rails forms important?
Forms are used frequently online and they are vital to our overall comprehension of how to work with Rails as it is your primary method for interacting with your app and, therefore, your data. While it is still possible to create pure HTML forms in Rails, extra steps would need to be taken so understanding the way Rails handles forms will save you time and numerous headaches.


#### How to set up form in Rails 

In order to create a functional form you need two controller actions (and two routes). One is for diplaying the form with all inputs and another is for submitting the form and saving data into database.  In Rails you will use:

- `new` and `create` actions for adding a new record to a database
- `edit` and `update` actions for modifying a record in a database

Read the [Forms for Creating New Model Records](https://human-se.github.io/rails-demos-n-deets-2020/demo-resource-create/) to understand the process for adding a new record to a database.

#### Form helpers
There are three form helpers you will come across, though two of them are being phased out in favor of the third. All are still valid, though the newest one, `form_with`, is able to handle what both of the previous two did and is naturally the one suggested for use.

##### Deprecated form helpers
While `form_tag` and `form_for` are only soft deprecated, going forward you will find them less and less. These were here before `form_with` and each had slightly different use cases. The biggest difference between them is that `form_for` takes a model whereas `form_tag` takes a URL.

- Read [this section](https://api.rubyonrails.org/classes/ActionView/Helpers/FormHelper.html#method-i-form_for) of the Rails API to see some examples of forms built with `form_for` and how to work with it.
- Read [this section](https://api.rubyonrails.org/classes/ActionView/Helpers/FormTagHelper.html#method-i-form_tag) of the Rails API to see some examples of forms built with `form_tag` and how to work with it.

##### form_with 
This is the form helper you will need to get the most comfortable with. It is versatile enough to use for any need and can take a URL, model, or scope. At its simplest we can create a form like this:
```ruby
<%= form_with model: @user do |form| %>
  <%= form.text_field :username %>
  <%= form.password_field :password %>
  <%= form.submit "Register" %>
<% end %>
```
which would translate to an HTML form similar to this:
```html
<form action="/users" method="post" data-remote="true">
  <input type="text" name="user[username]">
  <input type="password" name="user[password]">
  <input type="submit" value="Register">
</form>
```

- Read [this section](https://api.rubyonrails.org/classes/ActionView/Helpers/FormHelper.html#method-i-form_with) of the Rails API to see some examples of forms built with `form_with` and how to work with it.
- Read [this section](https://guides.rubyonrails.org/form_helpers.html#helpers-for-generating-form-elements) and [this section](https://guides.rubyonrails.org/form_helpers.html#other-helpers-of-interest) of the Rails guides to see some helpers provided for working with `form_with` and providing input types to your form.

#### Using partials
You will often notice that the form to create a record needs to be similar, if not identical, to the form for editing a record. This is an excellent opportunity to DRY your code by creating a partial.

Check out [this great tutorial](https://human-se.github.io/rails-demos-n-deets-2021/demos/form-partials/) for a walkthrough on setting up a form partial. Notice that it uses `bootstrap_form_with` instead of `form_with`, but they are the same it just gives some Bootstrap styling to the form. This `bootstrap_form_with` comes from the [bootstrap_form gem](https://github.com/bootstrap-ruby/bootstrap_form).

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
