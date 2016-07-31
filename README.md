# quick_master_ansible
1.5時間で戦士にするAnsible講習会


# 前提

* VirtualBox 5.0.26
* Vagrant 1.8.4
  * vagrant plugin install vagrant-vbguest

# 準備

```
vagrant up
```


# 確認

```
vagrant ssh ansible-server
ls /vagrant
exit
vagrant ssh www-server
ls /vagrant
exit
```

2台それぞれで ls /vagrant して、このリポジトリが見えていれば、OKです。
