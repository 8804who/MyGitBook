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

Flask에서는 return 문을 통해 요청에 대한 응답을 반환합니다. 이 return 문의 결과값은 단순한 문자열이 될 수도 있습니다. 하지만 더 복잡한 데이터 구조를 처리하기 위해서는 Flask의 helper function을 사용합니다. Flask의  helper function이란 개발자가 웹 개발 작업을 쉽게 할 수 있도록 도움을 주는 함수들로 _url\_fo&#x72;_&#xC774;나 _jsonify_ 같은 함수가 있습니다.

```python
@app.route('/json')
def json():
    return jsonify({" message": "Hi"})
```

위 코드는 helper function 중 _jsonif&#x79;_&#xB97C; 활용한 것으로 결과값을 JSON 형태로 반환해줍니다. 이때 Content-Type은 application/json으로 자동 설정되어 별 다른 처리 없이 클라이언트가 해당 결과값이 JSON 형태라는 것을 알 수 있게 해줍니다.

또한 응답의 status code나 header도 설정을 할 수 있습니다. 이를 수행하기 위해서는helper function 중 하나인 _make\_respons&#x65;_&#xB77C;는 함수를 사용합니다.

```python
from flask import Flask, make_response

@app.route('/response')
def response_example():
    resp = make_response("Hi", 200) # 여기서 Hi는 body, 200은 status code
    resp.headers['Custom-header'] = 'custom-value' # Custome-Header 값을 custom-value로 설정
    return resp
```

위와 같이 make\_response를 활용해 응답의 body, statud code, header를 직접 설정할 수 있습니다.

참고로 make\_response에 입력 가능한 매개 변수는 아래 코드와 같고 headers는 딕셔너리 형태로 설정 가능합니다.

```python
from flask import Flask, make_response

@app.route('/response')
def response_example():
    headers 내용 = {'X-Example': 'DirectHeader'}
    resp = body="body 내용", status="전송할 status code", headers="headers 내용")
    return resp
```
