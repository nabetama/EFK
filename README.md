# EFK

- Fluentd(td-agent)
- Kibana4
- ElasticSearch 1.7.2

## node1
踏み台
192.168.33.11

## node2
ElasticSearch,td-agent,Kibanaを動かす
それぞれサーバーを分けたければinventoriesとか書き換える
192.168.33.12

## First!

node同士の秘密鍵を合わせておく
```sh
$ vagrant ssh-config node1 > ssh_config
$ vagrant ssh-config node1 >> ~/.ssh/config
$ scp -F ssh_config .vagrant/machines/node2/virtualbox/private_key node1:.ssh/id_rsa
```
