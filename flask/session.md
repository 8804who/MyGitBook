---
description: Flask의 세션 활용
---

# Session

Session

세션은 서버 측에서 사용자의 상태  정보를 저장하여 사용하는 것으로 Flask에서도 쉽게 사용할 수 있습니다.

```python
from flask import Flask, session
app.secret_key = 'secret_key'
```

세션을 사용하기 위해서는 일단 위와 같이 secret key를 지정해 주어야합니다.&#x20;

```python
@app.route('/set_session')
def set_session():
    session['username'] = 'Lio'
    return '세션 설정 완료'
```

세션은 위와 같이 딕셔너리처럼 키와 값으로 정보를 저장할 수 있습니다. 이렇게 저장된 데이터는 사용자가 브라우저를 종료하거나 세션 유효 기간이 만료될 때까지 유지됩니다.

```
@app.route('/get_session')
def get_session():
    username = session.get('username')
    if username:
        return f'사용자 이름은 {username}입니다'
    else:
        return '사용자 이름이 설정되지 않았습니다.'
```

세션에 저장된 정보는 위와 같이 get 함수를 통해 접근할 수 있고 키가 존재하지 않는 경우 None 값을 반환합니다.

이외에도 여러 기능들이 있으며 대표적인 것을 몇 가지 아래에서 설명하겠습니다.

```
session.pop('username', None)
is_logged_in ='username' in session
session.clear()
```

pop 함수는 해당 키의 데이터를 가져온 후 삭제합니다. 두 번째로 들어간 인수는 해당 키의 데이터가 없을 때 반환 받을 값입니다.

'키 값' in session은 session 내에 해당 키 값이 존재하는지의 여부를 반환하므로 로그인 여부 등을 체크하는데 사용 가능합니다.

clear 함수는 세션 내의 모든 데이터를 삭제합니다.

