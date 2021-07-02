# Python Flask Tutorial: Full-Featured Web App Part 2 - Templates
[Video](https://www.youtube.com/watch?v=QnDWIZuWYW0)

## Import render template function
    from flask import render_template
    
## Return template
    @app.route("/home")
    def home():
        return render_template('home.html', posts=posts)
        
## Jinja for loop block
    {% for post in posts %}
        <h1> {{ post.title }} </h1>
        <p> By {{ post.author }} on {{ post.date_posted }} <p>
    {% endfor %}
        
## Jinja for if block
    {% if title %}
        <title>Flask Blog - {{ title }}</title>
    {% else %}
        <title>Flask Blog</title>
    {% endif %}
    
## Jinja for content block parent
    <div>
        {% block content %}{% endblock %}
    </div>
    
## Jinja for content block child
    {% extends "parent.html" %}
    {% block content %}
        Text
    {% endblock content %}

 ## Use an external CSS file
    from flask import url_for
    <link rel="stylesheet" type="text/css" href="{{ url_for('static', filename='main.css') }}">
 
 
