---
description: Flask의 Jinja2 template 활용 기능
---

# Template

### 템플릿을 활용한 로직 적용

Flask에서는 Jinja2라는 템플릿 엔진을 사용해서 변수, 반복문, 조건문 등을 포함하는 HTML 파일을 렌더링 할 수 있습니다.

```python
@app.route('/userpage')
def userpage(username):
    return render_template('userpage.html', username=username)
```

Flask에서는 위처럼 템플릿에 변수를 전달할 수 있고 아래와 같이 _\{{ 변수명 \}}으로 해당 변수를 불러올 수 있습니다._

```html
<p>유저명: {{ username }}</p>
```

참고로 Jinja2에서는 필터링이라는 기능을 제공하여 변수의 값을 필요에 따라 처리할 수 있으며 다음과 같은 필터들이 있습니다.

* safe: HTML 태그를 이스케이핑하지 않습니다
* capitalize: 문자열의 첫글자를 대문자로 변환합니다
* lower: 문자열을 소문자로 변환합니다
* upper: 문자열을 대문자로 변환합니다
* title: 문자열의 각 단어 첫 글자를 대문자로 변환합니다
* trim: 문자열 앞뒤 공백을 제거합니다
* striptags: 문자열에서 HTML 태그를 제거합니다
* truncate: 문자열을 특정 길이로 줄입니다
* date: datetime 객체를 문자열로 포맷합니다.

반복문과 조건문은 각각 아래와 같이 사용 가능합니다.

```html
<!-- 반복문 -->
<% for x in range(10) %>
    <p>{{ x }}</p>
<% endfor %>
```

```html
<!-- 조건문 -->
<% if lang == 'kor' %>
    <p>안녕</p>
<% elif lang == 'eng' %>
    <p>Hi</p>
<% else %>
    <p>?</p>
<% endif %>
```

### 매크로 기능

Jinja2에서는 매크로 기능을 지원하여 자주 쓸 기능을 아래와 같이 저장해놓고 불러와서 활용할 수 있습니다.

```html
<!-- macro.html -->
{% raw %}
{% macro 매크로명(변수)  %}
    <!-- 로직 -->
{% endmacro %}
{% endraw %}
```

```html
{% raw %}
{% from 'macro.html' import 매크로명 %}
{% endraw %}
    {{ 매크로명(입력할 변수) }}
```



### 템플릿 상속

Flask에서는 웹 페이지 개발의 효율성을 위해 템플릿을 상속하여 사용할 수도 있다.

```html
<!-- 상속할 템플릿 -->
<!-- main.html -->
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>main</title>
</head>

<body>
    <h1>contents</h1>
    {% raw %}
{% block 블록명 %}
    {% endblock %}
{% endraw %}
</body>

</html>
```

```html
<!-- 상속받을 템플릿 -->
{% raw %}
{% extends 'main.html' %}
{% block 블록명 %}
    <!-- 템플릿에 들어갈 내용 -->
{% endblock %}
{% endraw %}
```

위와 같이 상속할 템플릿 안에 _\{%  block 블록명 %\} \{% endblock %\}_&#xC73C;로 블록 구간을 지정해주고 상속 받을 템플릿에서 그 블록에 들어갈 내용을 입력합니다. 참고로 블록이 꼭 하나일 필요는 없으며 블록명을 다르게 지정해주며 여러 블록을 사용할 수도 있습니다.
