---
description: Flask의 요청 처리와 응답 처리
---

# Request & Response

### 요청 처리

Flask에서는 request 객체를 통해 요청 데이터에 접근 가능하며, 이 객체는 URL, 헤더, 쿠키, 쿼리 매개변수 등을 포함합니다.

```python
from flask import Flask, request

@app.route('/main')
def main():
    url = request.url # 해당 페이지의 URL 주소
    header = request.header # 해당 요청의 헤더
    cookies = request.cookies # 해당 요청의 쿠키
    args = request.args # 쿼리 매개변수
    return 'main'
```

위와 같이 request 객체를 통해 다양한 값을 받아올 수 있으며 쿼리 매개변수 args는 딕셔너리 형태로 이루어져 있습니다.

```python
from flask import Flask, request


@app.route('/login')
def login():
    username = request.form['username']
    return 'login'
```

또한 request 객체를 통하면 웹의 form에서 받아온 값들을 조회할 수도 있는데 위처럼 form에서 지정된 변수명을 통해서 값을 받아오는 방식입니다.

### 응답 처리



