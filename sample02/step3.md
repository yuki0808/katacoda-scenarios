## APMのセットアップ（Python）

以下コマンドを実行し、Flaskモジュールとロガーをインストール。
`pip install flask`{{execute}}

`pip install python-json-logger`{{execute}}

以下コマンドを実行して、Flaskのサンプルアプリをダウンロード。

`git clone https://github.com/yuki0808/flask-sample.git`{{execute}}

DatadogのTracerをインストール
`pip install ddtrace`{{execute}}

Webアプリケーションの起動
`ddtrace-run /usr/bin/python3 /root/flask-sample/run.py`{{execute}}

Terminalの+ボタンを押下し、`Select port to view on Host 1`を選択

![](https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/rRubbEDo/e49db587-310e-4d08-a436-e5a90d5ceb5c.jpg?v=d4ef05cf0eca0f621ed608914a879a4f)


新しく開かれたBrowserの画面でポート番号`8080`を入力し`Display Port`を押下。

![](https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/kpunnyvE/a93e138e-5b43-4453-8188-cac38d305312.jpg?v=d14ea1a84f62b784f03238b9abab643c)

参考資料:
https://docs.datadoghq.com/tracing/setup_overview/setup/python/?tab=containers
https://docs.datadoghq.com/tracing/connect_logs_and_traces/python/
