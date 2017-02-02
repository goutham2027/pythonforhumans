---
title: Changing defaults in Flask
categories: configuration flask
---

| Type                           | Default folder name |
|--------------------------------|---------------------|
| Static assets(CSS, JS, images) | static              |
| Templates (Jinja, HTML)        | templates           |
| Instance (configuration)       | instance            |

{% highlight python %}
from flask import Flask
from flask import render_template

app = Flask(__name__,static_folder='assets',template_folder='templates_007',instance_path="/full_path_to_instance_folder/instance_007", instance_relative_config=True)
app.config.from_pyfile('config.py')

@app.route("/")
def hello():
 print app.config["DEBUG"]
 return render_template('index.html')

if __name__ == "__main__":
 app.run(debug=app.config["DEBUG"])
{% endhighlight %}

For complete code check [github_repo](https://github.com/goutham2027/flask-code/tree/master/change_flask_default_folders)

Reference: [http://flask.pocoo.org/docs/0.10/api/](http://flask.pocoo.org/docs/0.10/api/)
