## ログの送信

2つ目のTerminal画面を開く。

![](https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/DOu6xKoD/ea7daed8-30ec-498c-8b99-0f507969d15e.jpg?v=e9fe2ef835884b9044242e0a3dabbf9b)


下記、Agentのコンフィグファイルを変更し、`logs_enabled`パラメーターを`true`に変更しログ機能を有効化。

`vi /etc/datadog-agent/datadog.yaml`{{execute}}

![](https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/ApuEkgYn/17bc9db9-1b82-4501-8bfb-d696cd7e83ff.jpg?v=477f5b839d8469946eae8e17a054a560)

```
logs_enabled: true
```

送信対象ログの情報を記載したコンフィグファイルを作成する。

`vi /etc/datadog-agent/conf.d/logs.yaml`{{execute}}

```
logs:
  - type: file
    path: /var/log/log.txt  
    service: flask
    source: python
```

以下のコマンドを実行し、Agentの再起動を行い設定を反映させる。
`sudo service datadog-agent restart`{{execute}}


設定が反映されて、Logが送信されているかStatusコマンドで確認する。

`sudo datadog-agent status`{{execute}}

![](https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/E0uKnLkE/1284eb63-98d7-4bda-a543-a10bca9a2532.jpg?v=52cad693b901f07f86be6a53a09082f3)

参考資料:
https://docs.datadoghq.com/logs/log_collection/?tab=host