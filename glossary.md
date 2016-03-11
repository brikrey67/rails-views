# Views and Controllers Glossary

#### Controller
> A collection of methods telling your Rails app how it should respond to each type of request.

#### `< ApplicationController`
> Every controller inherits from ApplicationController, similar to how every ActiveRecord model inherits from `ActiveRecord::Base`. The first line in any controller file will always be `class SomethingController < ApplicationController`.

#### Controller method
> One of the methods that tells your Rails app how it should respond to a specific type of request.

#### Action
> Another name for controller method.

#### Route
> One of the URLs your Rails app recognizes and to which it will respond with a controller method.

#### View
> Something your user sees as a webpage. Usually a `.html.erb` file.

#### `.html.erb`
> Like a regular HTML file, except you can put Ruby code snippets in it.

#### `ERB`
> Embedded Ruby -- Ruby code that's run from inside an HTML file

#### `<% some_code %>`
> aka "Clown Hats". A special sort-of-HTML-tag that tells your Rails app, "Hey, there's actually not HTML in here -- it's Ruby code." Will never be displayed to your users.

#### `<%= some_code %>`
> A code snippet that Ruby runs **and then** makes the result show up in your HTML, visible to your users.

#### `$ rake routes`
> A Terminal command that displays all the routes for your app.

#### `render`
> A method that tells a controller action if it should show a `.html.erb` and if so which one, or show JSON or plain text.

#### `redirect to:`
> A method that tells a controller action to redirect to a different URL instead of rendering a view.

#### Implicit rendering
> Controller actions by default look for views that have their name: `def wombat` will automatically render `wombat.html.erb` even if you don't include `render`.

#### Form
> An HTML tag that allows data to be submitted from a webpage.

#### `params`
> A hash of key/value pairs that are included with every request you make. It can include data included in a request's URL (/users/bilbo_baggins) or data submitted using a form on a webpage.

#### Strong params
> A method that allows only specific key/value pairs in `params` to be sent to your controller actions, for security purposes.

#### Partial
> A piece of `.html.erb` code that can be inserted into other `.html.erb` code.

#### `form_for @something do |f|`
> Generates an HTML `form` element for you.

#### `f.text_field :some_field`
> Generates an HTML `input` element for you such that, when you submit the form, `some_field: user_input` is one of the key/value pairs included in `params`.

#### `f.label :some_field`
> Generates an HTML `label` element for you such that, when you click on it, the `some_field` `input` element is highlighted.

#### `f.submit "My button text"`
> Generates a button that, when clicked, submits the data the user entered into the `form` and loads the URL to which the data was sent.

#### GET
> A type of HTTP request that is conventionally used only to *retrieve and read* data, not to *send and change* data.

#### POST
> A type of HTTP request that is conventionally used to *send and change* data.

#### index route
> Conventional name for a route used to display multiple records of a certain class (e.g. multiple users)

#### show route
> Conventional name for a route used to display a single record of a certain class (e.g. one user)

#### new route
> Conventional name for a route used to display the `form` to create a new record of a certain class (e.g. a "Sign Up" page for users)

#### edit route
> Conventional name for a route used to display the `form` to update an existing record of a certain class (e.g. "Edit your profile" page for users)

