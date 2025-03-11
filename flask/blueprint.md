---
description: Blueprint를 활용한 Flask의 모듈 관리
---

# Blueprint

### Flask의 모듈 관리

Flask에 프로젝트를  진행하면서 코드가 길어지고 함수가 많아지면 이 모든 것을 하나에 저장해서는 관리를 하기 쉽지 않을 것입니다. 따라서 Flask에서는 Blueprint라는 것을 통해 파일을 분리하고 관리합니다.

```python
from flask import Flask
from . import file1

app = Flask(__name__)

app.register_blueprint(bp, url_prefix="/file1")
```

<pre class="language-python"><code class="lang-python"><strong># file1.py
</strong><strong>from flask import Blueprint
</strong>
bp = Bluepoint("file", __name__)

@bp.route("/func1")
def func1():
    return "result"
</code></pre>

위처럼 Bluepoint를 지정하고 이를 등록할 수 있습니다. Bluepoint 등록에서 인수로 사용된 url\_prefix는 해당 Bluepoint의 주소를 호출할 때 들어가는 접미사로 file1의 func1을 호출하려면 /file1/func1으로 요청을 해야합니다.

