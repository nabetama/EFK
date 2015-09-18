# EFK

- ElasticSearch
- Fluentd
- Kibana
- ServerSpec

## node1
192.168.33.11

## node2
192.168.33.12

## First!

node同士の秘密鍵を合わせておく
```sh
$ vagrant ssh-config node1 > ssh_config
$ vagrant ssh-config node1 >> ~/.ssh/config
$ scp -F ssh_config .vagrant/machines/node2/virtualbox/private_key node1:.ssh/id_rsa
```
