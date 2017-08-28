# Ansible Role: Logstash

Ansible role for installing Logstash on CentOS

## Requirements
Oracle JVM 1.8u40+

or

IcedTea OpenJDK 1.8.0.91+

## Variables
|Variable Name | Default Value |
|:------------|:-------|
`ls_yum_repo_baseurl` | `https://artifacts.elastic.co/packages/5.x/yum`
`ls_yum_repo_gpgkey` | `https://artifacts.elastic.co/GPG-KEY-elasticsearch`
`ls_node_name` | [`inventory_hostname`](http://docs.ansible.com/ansible/latest/playbooks_variables.html#magic-variables-and-how-to-access-information-about-other-hosts)
`ls_data_path` | `var/lib/logstash`
`ls_config_path` | `/etc/logstash/conf.d`
`ls_log_path` | `/var/log/logstash`
`ls_network_host` | `127.0.0.1`
`ls_http_port` | `9600`
`es_hosts` | `- 'localhost:9200'`

## Usage
```
roles:
  - role: erumble.logstash
    ls_network_host: 0.0.0.0
```
