# hobo.ansible.nginx_ssl_reverse_proxy
Configure a basic ssl reverse proxy server for nginx

## Installation
[Ansible Galaxy](https://galaxy.ansible.com/docs/using/installing.html) can be used to install the role:

`ansible-galaxy install git+https://github.com/hobointhecorner/hobo.ansible.nginx_ssl_reverse_proxy.git[,<branch or commit hash>]`

## Variables
|           Name            |  Type  | Required | Default | Description |
|---------------------------|--------|----------|---------|-------------|
| nginx_redirect_config_dir | string | **yes**  |         | Directory in which the nginx server configuration file will be stored |
| nginx_redirect_hostname   | string | **yes**  |         | nginx `server_name` to listen for |
| nginx_redirect_url        | string | **yes**  |         | URL to which traffic should be redirected |
| nginx_redirect_cert_path  | string | **yes**  |         | Path to where the listener SSL certificate is stored |
| nginx_redirect_key_path   | string | **yes**  |         | Path to where the listener SSL private key is stored |
| nginx_redirect_owner      | string | **yes**  |         | User applied as `owner` permissions to configuration files created by this role |
| nginx_redirect_group      | string | **yes**  |         | Group applied as `group` permissions to configuration files created by this role |
| nginx_redirect_port       | number |    no    |   443   | Port to listen on |
| nginx_redirect_mode       | string |    no    |   755   | Permissions to apply to configuration files created by this role |
