# Python Flask Tutorial: Full-Featured Web App Part 1 - Getting Started
[Video](https://www.youtube.com/watch?v=MwZwr5Tvyxo&list=PL-osiE80TeTs4UjLw5MM6OjgkjFeUxCYH)

## Install Flask
    pip install flask
    
## Create Flask app 
    from flask import Flask
    app = Flask(__name__)
    
## Create Flask routes
    @app.route("/")
    @app.route("/home")
    def home():
        return "<h1>Home Page</h1>"
    
    @app.route("/about")
    def about():
        return "<h1>About Page</h1>"
    
## Run Flask app from terminal
    export FLASK_APP=flaskapp.py
    flask run
    
## Run Flask in debug mode
    export FLASK_DEBUG=1
    
## Run Flask from script with debug mode
    if __name__ == '__main__':
        app.run(debug=True)
        
        
