# MVC with Flask
- install flask
```pip install flask```
  
- create app.py

- Import flask
```from flask import Flask, render_template```
- creating an app instance
```app = Flask(__name__)```
- use a decorator `@` to define the route for our web page
```@app.route("/")```
- setting up a default page
```
def index():
    return "Welcome to DevOps team"
```
- creating more pages
```
@app.route("/welcome/")
def welcome():
    return f"Welcome on board"

@app.route("/home/")
def home():
    return render_template("index.html")

@app.route("/feature/")
def feature():
    return render_template("feature.html")

@app.route("/about/")
def about():
    return render_template("about.html")
```
- Allowing the programmer to have control over the python script.
```
if __name__ == "__main__":
    app.run(debug=True)
```
- `debug=True` shows any errors