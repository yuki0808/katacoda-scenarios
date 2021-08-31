## Agentのインストール

次のコマンドを実行してホスト名を変更してください。

`hostname <YOUR_HOST_NAME>`

`hostname`コマンドを実行して、ホスト名が変更されたか確認してください。

以下のワンライナーコマンドを実行してAgentインストール。

`DD_AGENT_MAJOR_VERSION=7 DD_API_KEY=<YOUR_API_KEY> DD_SITE="datadoghq.com" bash -c "$(curl -L https://s3.amazonaws.com/dd-agent/scripts/install_script.sh)"`

これにより、Datadog Agent用のAPTパッケージがインストールされ、パスワードの入力を求められます。
エージェントがまだマシンにインストールされておらず、インストール後に自動的に起動させたくない場合は、上記のスクリプトの前に DD_INSTALL_ONLY=true を付けてから実行してください。