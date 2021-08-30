Run the command to change hostname:

`hostname <YOUR_HOST_NAME>`

Run the command `hostname` to confirm that the hostname was changed.

Use our easy one-step install.

`DD_AGENT_MAJOR_VERSION=7 DD_API_KEY=<YOUR_API_KEY> DD_SITE="datadoghq.com" bash -c "$(curl -L https://s3.amazonaws.com/dd-agent/scripts/install_script.sh)"`

This will install the APT packages for the Datadog Agent and will prompt you for your password.
If the Agent is not already installed on your machine and you don't want it to start automatically after the installation, just prepend DD_INSTALL_ONLY=true to the above script before running it.
