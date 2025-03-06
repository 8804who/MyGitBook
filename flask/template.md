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

반복문과 조건문은 각각 아래와 같이 사용 가능합니다.

```html
# 반복문
<% for x in range(10) %>
    <p>{{ x }}</p>
<% endfor %>
```

```html
# 조건문
<% if lang == 'kor' %>
    <p>안녕</p>
<% elif lang == 'eng' %>
    <p>Hi</p>
<% else %>
    <p>?</p>
<% endif %>
```

### 템플릿 상속

