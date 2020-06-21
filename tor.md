### Tor

Tor listens for all requests on port 9050

```sh
$ ss -nlt
```

Check my external IP address

```sh
$ wget -qO - https://api.ipify.org; echo
```

Check my external IP address use the torsocks

```sh
$ torsocks wget -qO - https://api.ipify.org; echo
```

Torify my shell

```sh
$ source torsocks on
$ source torsocks off
```

Change permanent for all your new shell sessions

```sh
$ echo ". torsocks on" >> ~/.bashrc
$ echo ". torsocks off" >> ~/.bashrc
```

To disable Tor for your current shell 

```sh
$ source torsocks off
```

## important

Restart Tor to apply changes:
```sh
$ sudo /etc/init.d/tor restart
```


Enable Tor Control Port

```sh
$ torpass=$(tor --hash-password "my-tor-password")
```

#### link https://linuxconfig.org/install-tor-on-ubuntu-18-04-bionic-beaver-linux

