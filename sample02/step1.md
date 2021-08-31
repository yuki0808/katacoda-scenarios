Run the command to change hostname:<br>
次のコマンドを実行してホスト名を変更してください。

`hostname <YOUR_HOST_NAME>`

Run the command `hostname` to confirm that the hostname was changed.<br>
`hostname`コマンドを実行して、ホスト名が変更されたか確認してください。

Use our easy one-step install.<br>
以下のワンライナーコマンドを実行してAgentインストール。

`DD_AGENT_MAJOR_VERSION=7 DD_API_KEY=<YOUR_API_KEY> DD_SITE="datadoghq.com" bash -c "$(curl -L https://s3.amazonaws.com/dd-agent/scripts/install_script.sh)"`

This will install the APT packages for the Datadog Agent and will prompt you for your password.
If the Agent is not already installed on your machine and you don't want it to start automatically after the installation, just prepend DD_INSTALL_ONLY=true to the above script before running it.<br>
これにより、Datadog Agent用のAPTパッケージがインストールされ、パスワードの入力を求められます。
エージェントがまだマシンにインストールされておらず、インストール後に自動的に起動させたくない場合は、上記のスクリプトの前に DD_INSTALL_ONLY=true を付けてから実行してください。