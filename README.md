# EFK

- ElasticSearch
- Fluentd
- Kibana
- ServerSpec

## First!

node同士の秘密鍵を合わせておく
```sh
$ scp -F ssh_config .vagrant/machines/node2/virtualbox/private_key node1:.ssh/id_rsa
```
