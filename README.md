
### Repository Modifications 

| Files             |  Content                                   |
|----------------------|--------------------------------------------|
| `requirements.txt`           | Added requirement.txt in order for Azure to build the app with Oryx since it looks for a requirements.txt to build all dependencies              |
| `api.py -> app.py`       | Renamed to account for Azure Startup - Azure only looks for app.py or application.py with Flask during startup                       |
| `app.py`               | ```nltk.download('popular')
import ssl
try:
    _create_unverified_https_context = ssl._create_unverified_context
except AttributeError:
    pass
else:
    ssl._create_default_https_context = _create_unverified_https_context  ```|
    
    
    ```nltk.download('popular')
import ssl
try:
    _create_unverified_https_context = ssl._create_unverified_context
except AttributeError:
    pass
else:
    ssl._create_default_https_context = _create_unverified_https_context  
    
    ```


Created Date: 30 Jan 2019
# NLP-Flask-Website
<b>static folder</b> contains all the CSS and images<br>
<b>template folder</b> contains all the HTML pages<br>
<b>api.py</b> file contains all the route to HTML pages and python scripts<br>
<b>Note:</b> if you want don't know much about FLASK and webapp, go through : https://medium.com/@pemagrg/build-a-web-app-using-pythons-flask-for-beginners-f28315256893


# To Execute
1. run ```api.py```
2. open the url that it gives you after you run the code
3. Tada!! the web app will open!

Still confused as to how to run?<br>
Well, then open your terminal,<br>
```
cd <path/to/your/project>
$python api.py<br>
```
it will give a link to open<br>
click and the web app will be open in your Web browser.

<br>
# Creating a Flask Website for NLP <br>

![nlpgif](NLPFlask.gif)
