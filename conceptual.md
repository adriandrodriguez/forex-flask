### Conceptual Exercise

Answer the following questions below:

- What are important differences between Python and JavaScript?
  A: JavaScript can be used and processed on the front-end and back-end. Python is processed onyl on the server-side.
  Instead of using brackets, like JavaScript, Python uses indentations to define code blocks.
  Python also uses many external libraries.

- Given a dictionary like `{"a": 1, "b": 2}`: , list two ways you
  can try to get a missing key (like "c") _without_ your programming
  crashing.
  A: Two ways are: One, use get(key,def_val) and check for a key and if its not there the return a message: my_dict.get('c', 'Not Found')
  Two: Use setdefault(key, def_value) if a key in not found, a new key is created with defined and default value: my_dict.setdefault('c', 'Not Found')

- What is a unit test?
  A: A unit test runs a test on a part of the code, it does not test the whole code like end-to-end. A unit test could test functions, class, or a particular method.

- What is an integration test?
  A: An integration test, tests multiple components of an app to make sure everything is working together.

- What is the role of web application framework, like Flask?
  A: Flask and other similar frameworks make server-side scripting usable to render the front-end. Flask also allows users to create routes, HTML templates, and use CSS and JavaScript while using Python as the primary programming language.

- You can pass information to Flask either as a parameter in a route URL
  (like '/foods/pretzel') or using a URL query param (like
  'foods?type=pretzel'). How might you choose which one is a better fit
  for an application?
  A: When a user uses the URL (/foods/pretzel) Flask creates a route to this specific route. If this route is not defined, then the server will pass error code 404 in the header. The second URL (foods?type=pretzel) follows the food route and passes in a vlaue of pretzel into the type variable.

- How do you collect data from a URL placeholder parameter using Flask?
  A: You collect the parameter when setting up the URL route in the Flask app. The user creates a parameter surrounded by <> signs. To collect the id for a page you write the route like so:

<!-- @app.route('/foods/<type>')
  def food_page(type): -->

- How do you collect data from the query string using Flask?
  A: To return the full query string, a user will import the request object from flask and then use return request.query_string. To access individual known parameters you would use the args method: return request.args.get('param')

- How do you collect data from the body of the request using Flask?
  A: Step one: import the request object from Flask library: from flask import request and get user input information through a form, you will submit a POST request and store the information in a variable.

- What is a cookie and what kinds of things are they commonly used for?
  A: Cookies are tiny text files with various pieces of data. They are often used to identify specific information about users related internet usage.

- What is the session object in Flask?
  A: Session objects track the session data through a dictionary that contains a key-value pair for the associated session. Sessions also store data similar to cookies, but the data is gone once the session is over, and is not used on the local storage of a computer.

- What does Flask's `jsonify()` do?
  A: This creates a response in JSON format; it unpackages the information when recieived by the user:

<!-- from flask import jsonify
@app.route('/get_user_info)
def get_user_info():
      return jsonify(username=user.username, email=user.email, id=user.id) -->
