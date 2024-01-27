# Request specs

First things first, let's get on the same page. You might have seen mentions of a "controller spec" around the internet, this is an old concept of Rails and no longer encouraged. These days you deal with request specs or system/integration specs. Here we are going to focus on request specs which are the closest to the old controller specs.

In Rails, these request specs are considered functional tests of your controllers. This is because you are testing how your actions (controllers) handle the requests and the expected result or response, in some cases an HTML view.

## Working with controllers

Controllers are classes, like models. You may not have thought much about it because Rails creates a new instance of controller classes for us, and we tend to think of them as actions.

Controllers are unique types though because they function inside of a request/response cycle. They expect the browser to send them a request then they put together a response to send back. Controllers are also in charge of:

- Redirecting actions
- Setting values for cookies & sessions
- Rendering templates

### Rspec helpers

Rspec provides the following helpers to make requests

- `get(path, options)`
- `post(path, options)`
- `patch(path, options)`
- `put(path, options)`
- `delete(path, options)`

The methods’ first argument should be the `path` of the action you want to test, remember to check with `rails routes` in case you don't remember the helper for the path. The `option` is the hash of any other values you want to pass.

```ruby
# GET request
get users_path

# POST request with params
post(users_path, params: { user: {first_name: 'Uduak', last_name: 'Essien'}})
```

### Helpers after a request

After a request is made you will have a couple of other helpers available

- `cookies`: Hash containing any cookies that are set
- `flash`: Hash containing any objects living in the flash
- `session`: Hash containing any object living in session variables
- `controller`: The controller processing the request
- `request`: The request object
- `response`: The response object

## Writing a request spec

Make sure you have already installed [rspec-rails](https://github.com/rspec/rspec-rails) and then we can proceed to scaffold a `user`

```
bin/rails generate scaffold user first_name:string last_name:string
```

You now will have a spec pre-made by the scaffolding, open the file `spec/requests/users_spec.rb`. In this file, you will have a lot of different specs, but let's take a look at some of them and go by the things happening.

Remember that if you want to run the specs you can do `rspec spec/requests/users_spec.rb`

```ruby
describe "GET /show" do
  it "renders a successful response" do
    user = User.create! valid_attributes #1
    get user_url(user) #2
    expect(response).to be_successful #3
  end
end
```

Here we can see the following happening:

1. `User.create!` creates a user for the test with `valid_attributes` as attributes
2. `get user_url(user)` performs a GET request to the user show action
3. `expect(response).to be_successful` we check that the response was good, but not its contents

```ruby
describe "POST /create" do
  context "with valid parameters" do
    it "creates a new User" do
      expect {
        post users_url, params: { user: valid_attributes } #2
      }.to change(User, :count).by(1) #1
    end

    it "redirects to the created user" do
        post users_url, params: { user: valid_attributes }
        expect(response).to redirect_to(user_url(User.last)) #3
      end
  end
end
```

Here we can see the following happening:

1. `expect {...} .to change(User, :count).by(1)` our test expects the `User` count to change by 1
2. `post users_url, params: { user: valid_attributes }` performs a POST request to `user_url` passing the params with user valid attributes to try and create one
3. `expect(response).to redirect_to(user_url(User.last))` expects the POST request to result in a redirection to a user show URL for the newest user

## Conclusion

As you might see, the request spec now deals with making a request, the side effects of it, and the response. The actual flow of things should not be tested here, it belongs in a system/integration spec.


