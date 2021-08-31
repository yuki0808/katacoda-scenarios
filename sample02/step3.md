

`pip install flask`{{execute}}

run.py

```
from flask import Flask
app = Flask(__name__)
 
@app.route('/')
def hello_world():
    return '<html><body><h1>Hello world!</h1></body></html>'
 
if __name__ == '__main__':
    app.run(host='0.0.0.0', port=8080)
```

`pip install ddtrace`{{execute}}

`ddtrace-run /usr/bin/python3 run.py`{{execute}}

Terminalの+ボタンを押下し、`Select port to view on Host 1`を選択

![](https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/rRubbEDo/e49db587-310e-4d08-a436-e5a90d5ceb5c.jpg?v=d4ef05cf0eca0f621ed608914a879a4f)


新しく開かれたBrowserの画面でポート番号`8080`を入力し`Display Port`を押下。

![](https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/kpunnyvE/a93e138e-5b43-4453-8188-cac38d305312.jpg?v=d14ea1a84f62b784f03238b9abab643c)
