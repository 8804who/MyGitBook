---
description: Flask의 라우팅 기능과 관련 기능
---

# Routing

### 라우팅

Routing은  어떤 주소에 어떤  기능을 매핑할 지 정하는 것으로 **@app.route("URL 주소")** 형식으로 지정 가능합니다. 별 다른 로직 없이 단순히 데코레이터를 적용하는 것으로 편하게 사용할 수 있습니다.

```python
@app.route("/main")
def main():
    return "main_page!"
```

위 코드는 main이라는 함수를 _/mai&#x6E;_&#xC774;라는 URL 주소에 매핑한 것으로 사용자가 URL 창에 _/mai&#x6E;_&#xC744; 입력하면 해당 함수의 결과를 받아와서 페이지에 출력해줍니다.

### URL 변수

변수 값을 받아와서 URL 주소 내에서 사용할 수도 있습니다.

```
@app.route("/userpage/<username>
def userpage(username):
    reutnr "user_page"
```

위 코드는 username이라는 변수를 URL 주소내에서 사용하는 것으로 이런 방식으로 유저 별 페이지를 작성할 수도 있습니다.

### HTTP 메서드

HTTP 메서드를 지정할 때는&#x20;

```
@app.route("/address",method=['GET'])
```

형식으로 지정합니다.

메서드를 지정하지 않을 경우 기본적으로는 GET 방식으로 통신을 수행합니다.

또한하나의 함수에서 여러 HTTP 메서드를 사용할 수도 있는데 이때는

```
@app.route("/address",method=['GET','POST']
def method():
    if request.method == "GET":
        return "It's GET"
    if request.method == "POST":
        return "It's POST"
```

형식으로 사용합니다. 이때 _reuqest.method_ 변수는 해당 요청의 HTTP 메서드로 요청의 종류에 따라 반환값을 지정할 수 있습니다.

### URL 빌더

URL 빌더를 활용하면 함수명으로 간편하게 해당 함수에 매핑되어있는 URL 주소를 받아올 수 있습니다.

해당 방식을 이용하면 함수명으로  URL 주소를 받아오기 때문에 특정 페이지의 URL 주소를 변경하더라도 해당 페이지와 연계되어 있는 함수들을 일일이 수정해야 할 필요가 없어집니다.

```
function1_url = url_for("function1")
```

위 코드는 URL 빌더의 예시로 **function1\_url**이라는 변수에 **function1** 함수에 매핑된 URL 주소를 받아와서 저장합니다.

그리고 지정된 URL 주소로 이동하는 _redirect_ 함수와 함께 사용하면 해당 페이지로 이동하는 기능도 구현할 수 있습니다.

```
@app.route("/function1")
def function1():
    return redirect(url_for("function2")
```

위와 같이 코드를 작성하면 function1이라는 페이지에 접속했을 때 function2 페이지로 자동으로 이동하게 됩니다.

또한 아래처럼 변수를 전달할 수도 있고 절대 URL이나 https UR 반환 받을 수도 있습니다.

```
url_for("userpage", username=username) # 변수 전달
url_for("function1", _extrenal=True) # 절대 URL 반환
url_for("function1", _scheme='https', _external=True) # HTTPS URL 반환
```

여기서 절대 URL이란 _http://127.0.0.1:5000/function&#x31;_&#xCC98;럼 도메인을 포함한 전체 URL입니다.

### 타입 힌트

Flask에서는 URL 주소에도 타입 힌트를 사용 할 수 있습니다.

```
@app.route("/address/<int:num1>/<int:num2>")
```

위의 형식으로 타입 힌트를 사용할 수 있으며 파이썬의 타입 힌트에서는 해당 타입이 들어오지 않아도 함수가 동작하지만 Flask에서는 해당 타입 대신 다른 타입의 변수가 들어오면 404 에러가 발생합니다.

Flask에서 사용 가능한 대표적인 타입 힌트의 종류는 아래와 같습니다.

* string (디폴트): 어떤 텍스트도 가능하지만 슬래시(/)는 제외
* int: 정수
* float: 부동 소수점 숫자
* path: 슬래시(/)를 포함한 문자열
* uuid: UUID 문자열
