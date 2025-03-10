---
description: Flask에서의 static file 활용
---

# Static Files

### Static File 다루기

Static file이란 웹 서버가 별 다른 처리 없이 그대로 전달해주는 파일입니다. 주로 이미지, CSS, 자바스크립트 같은 리소스들이 이에 해당합니다.\
Flask에서는 이런 static file들을 아래와 같이 static이라는 폴더에 저장하여 관리합니다.

```
├─ app.py 
├─ templates 
│  └─ index.html 
└─ static
   ├─ js
   │   └─ main.js
   ├─ css
   │   └─ style.css
   └─ img
       └─ image.jpg
```

### Static file 경로 관리

Flask에서는 static file의 경로를 여러가지 방식으로 관리할 수 있습니다.\
불러올 해당 static file의 절대 경로를 통해 관리할 수도 있고 아래처럼 _url\_for_ 함수를 이용해 경로를 관리할 수도 있습니다.

```python
# app.py
from flask import Flask, render_template

app = Flask(__name__)

@app.route("/")
def home():
    return render_template("index.html")
```

```html
<!-- index.html -->
<!DOCTYPE html>
<head>
    <meta charset="UTF-8">
    <title>Flask Static File</title>
</head>
<body>
    <img src="{{ url_for('static', filename='img/image.jpg') }}">
</body>
</html>
```

위  코드의 _url\_for('static', filename='/img/image.jpg')_&#xC740; flask 프로젝트의 static 폴더의 주소를  가져온 후 그 뒤에 파일 경로를 붙여서 그 주소를 반환합니다.

참고로 static 폴더의 기본 주소는 /static이지만 아래와 같이 직접 설정할 수도 있습니다.

```python
from flask import Flask

app = Flask(__name__, static_url_path='/custom_static')
```

만약 절대 경로를 통해 static file을 관리했다면 위의 코드에서 static 폴더의 경로가 바뀌면 모든 절대 경로를 일일이 수정해주어야 하지만 _url\_for 함수를 통해 관리할 경우 그럴 필요가 없습니다._

또 다른 방법으로는 아래와 같이 원하는 경로에  대한 요청을 _static_ 폴더 내 경로로 리디렉션하여 처리하는 방법도 있습니다.

```python
from flask import Flask

app = Flask(__name__)

@app.route('/img/<path:filename>')
def img(filename):
    return send_from_directory('static/img', filename)
```

