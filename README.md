
# [SSH-MITM Server](https://github.com/ssh-mitm/ssh-mitm)


**SSH-MITM is a man in the middle (mitm) server for security audits supporting public key authentication, session hijacking and file manipulation.**

## Installation SSH-MITM

<img src="https://www.ssh-mitm.at/assets/images/streamline-free/monitor-loading-progress.svg" align="left" width="138">

The first step to using any software package is getting it properly installed.

To install SSH-MITM, simply run this simple command in your terminal of choice:

    $ flatpak install at.ssh_mitm.server

## Connect to the network

<img src="https://www.ssh-mitm.at/assets/images/streamline-free/programmer-male.svg" align="left" width="138">

To start an intercepting mitm-ssh server on Port 10022, all you have to do is run a single command.

```bash
# start the mitm server
$ flatpak run at.ssh_mitm.server --remote-host 192.168.0.x

# connect to the mitm server
$ ssh -p 10022 user@proxyserver
```

## Hijack SSH sessions

<img src="https://www.ssh-mitm.at/assets/images/streamline-free/customer-service-woman.svg" align="left" width="138">

When a client connects, the ssh-mitm starts a new server, which is used for session hijacking.

```
[INFO] created injector shell on port 34463
```

To hijack this session, you can use your favorite ssh client. All you have to do is to connect to the hijacked session.

```bash
$ ssh -p 34463 127.0.0.1 
```


## Contributing

<img src="https://www.ssh-mitm.at/assets/images/streamline-free/write-paper-ink.svg" align="left" width="138">

Please contribute to [SSH-MITM server](https://github.com/ssh-mitm/ssh-mitm)

**Pull requests are welcome.** 

For major changes, please open an issue first to discuss what you would like to change.
