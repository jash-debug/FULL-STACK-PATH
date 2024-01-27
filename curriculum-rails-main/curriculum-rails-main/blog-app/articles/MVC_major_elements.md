
### The Model
##### In General
The Model can be thought of as the data access point. Sometimes it is actually a database, sometimes it is just a JSON file. You may have referred to it as a 'store' at some point, or even seen something like this:  
```js
const something = {
    attribute1: 'true',
    attribute2: false,
    attribute3: [
            {
                set1: 1,  
                set2: 'hello'
            },
            {
                set1: 2,
                set2: 'world!'
            }
        ]
    }
```  
As a data access point, you already have plenty of experience with the Model.

##### In Rails
Technically the Model is what you go through to interact with the database and it is known as the ActiveRecord. It is where you write your rules, validations, scopes, and other functions necessary when interacting with your data. Your Model is the actual line that connects your database, such as PostgreSQL, to your Controller.

### The View
##### In General
The View should feel very comfortable to you by now. This is your front-end. This is where you put your HTML, any classes for your SCSS, or a CSS framework like Bootstrap. In some programming languages you can compile the HTML through that language like with React components. In any case, the View is always going to refer to what the User gets to see and interact with.

##### In Rails
This time your HTML will have embedded Ruby (erb) using <% %> tags around the Ruby code. This is also how you will display any variables made available to you through the corresponding Controller. You may recall seeing something like this:  
```html
<h1>{'Hello World!'}</h1>
```  
Well, now we're going to use this:  
```html
<h1><%='Hello World!'%></h1>
```
 to do the same thing.
 
 Do you know the difference between `<% %>` and `<%= %>`? In a nutshell - the first one only executes the code, the other also prints the output. Read the detailed description [here](https://api.rubyonrails.org/classes/ActionView/Base.html).

### The Controller

##### In General
The Controller is what handles the internal routing of your project. This is the key to your MVC architecture, as it stands between the Model and the View, directing the flow of data as your Users request it. It is common for many different stacks to use RESTful conventions and the Controller is where the REST happens!

##### In Rails
It is as closely linked to the routes.rb file as the Model is linked to the database. As such, it is where your routes are actually pointing. From inside the controller, you have all the control. You say what goes where. This is, primarily, where you will call data from the Model to display to the View.

As data comes in from the outside world, it hits the routes.rb file first. This routes file sends traffic to the controller#action called for in the route. That request will then be available to the corresponding action with data attached as params. Once you have the data in your Controller method, you can manipulate it as needed and return what data is required. Sometimes that's going to be JSON or XML, sometimes it's going to be an erb layout with that data on the page. This is what makes Rails such a powerful tool for building APIs and Web Apps alike.

