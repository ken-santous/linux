### Ubuntu

List all services in Ubuntu.

```sh
$ service --status-all
```

Use Systemd to Stop/Start/Restart/Check Services in Ubuntu.

```sh
$ sudo systemctl stop ufw
$ sudo systemctl start ufw
$ sudo systemctl restart ufw
$ sudo systemctl status ufw
```

Using Init scripts to manage services

```sh
$ /etc/init.d/ufw stop
$ /etc/init.d/ufw start
$ /etc/init.d/ufw restart
$ /etc/init.d/ufw status
```

Systemctl disable/enable name_of_service.service 

```sh
$ sudo systemctl disable tor.service
$ sudo systemctl enable tor.service
```
Systemctl unmask name_of_service.service 

```sh
$ sudo systemctl unmask mysql
$ sudo systemctl mask mysql
```


List unit files

```sh
$ sudo systemctl list-unit-files
```


# Dillinger website
