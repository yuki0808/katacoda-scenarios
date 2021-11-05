## Agentの操作

Agentが正しく実行されているか以下のコマンドをTerminalで実行。
本コマンドを実行することでDatadogのAgentやインテグレーションのステータスの確認が可能。

`sudo datadog-agent status`{{execute}}


以下のコマンドを実行し、Agentのコンフィグファイルを開き、ホストに任意のタグ情報を付与。
`vi /etc/datadog-agent/datadog.yaml`{{execute}}

コンフィグファイル内にタグを設定する項目があるので、その箇所に任意のタグ情報を追加する。

![](https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/7KuALjxe/46ddd4f7-27c0-4b86-86f9-5bd7859f82c9.jpg?v=abbc9a0dae56a83d34d3327e36c9fbd6)

`env:test`環境用のタグを追加。

```
tags:
  - env:test
```

![](https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/WnukJ6Zq/5e42526c-92cd-4145-b970-cd46973dfbe7.jpg?v=757b9cda1111cb0beab6c085f8e3f74f)


以下のコマンドを実行し、Agentの再起動を行い設定を反映させる。
`sudo service datadog-agent restart`{{execute}}

Datadogの以下の画面(Host map)にアクセスしAgentをインストールしたホストの情報が表示されているか確認。

https://app.datadoghq.com/infrastructure/map

![](https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/RBuEOBXB/23e0ccd8-b128-4429-bf06-40c1da1f5549.jpg?v=d2d9cffe60ecd06af24b3364f13a7668)

参考資料:
https://docs.datadoghq.com/agent/basic_agent_usage/?tab=agentv6v7