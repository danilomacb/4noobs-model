[Roadmap](../../../README.md)

```py
from flask import Flask

app = Flask(__name__)

@app.route('/')
def homepage():
 return '<h1>Ola Mundo!</h1>'

app.run(debug=True)
```
