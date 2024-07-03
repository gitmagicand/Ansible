# Ansible basics

Подробная документация доступна по ссылке [Ansible](https://docs.ansible.com/ansible/latest/index.html).


## [Install Ansible on Ubuntu](https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html#installing-ansible-on-ubuntu)

Устанавливаем ```ansible``` командами
```sh
$ sudo apt update
$ sudo apt install software-properties-common
$ sudo add-apt-repository --yes --update ppa:ansible/ansible
$ sudo apt install ansible
```
Проверяем установку:

```sh
$ ansible --version
```

Получаем список хостов для работы ```ansible``` :
```sh
$ ansible all --list-hosts -i hosts.ini
```

Выполняем команду "ping" на хостах. Если в hosts.ini добавить параметры ansible_user и ansible_password
(```hosts.ini``` --> ```192.168.10.15 ansible_user=user ansible_password=password```)
, то ключ --ask-pass можно опустить:
```sh
$ ansible all -i hosts.ini -m ping --ask-pass
```

код вставки картинки
<p align="left">
  <img src="./image-2.jpg" height="80" title="image_from_dockerhub">
</p>
