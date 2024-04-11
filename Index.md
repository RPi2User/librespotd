# Librespot-Service

Quick and dirty solution to deamonize Librespot.
Librespot is the back-bone of every Linux-Solution that claimes to interact via Spotify-Connect.

I highly suggest, that you use Raspotify instead librespotd.

This Project is there to get myself comfortable in handling systemd-Services.

## Install

In Order to install Librespot you need to provide the Dependencies.  
Those dependencies are split up into, those you need for building the Project and those you need to install rust.
After the dependencies are all met, you can install librespot

### Dependencies

Install the Dependencies for rust:

```bash
root@raspi:~# apt install libasound2-dev portaudio19-dev build-essential libpulse-dev libdbus-1-dev
```

Install [rust](https://www.rust-lang.org/tools/install):

```sh
root@raspi:~# curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

[CTRL+D] out of the Session and reastablish the Connection.

### Deploy `librespot.sh`

### Setting up the Systemd-Service

1. Paste `librespot.service`-file into `/etc/systemd/system/` (It should result into `/etc/systemd/system/librespot.service`)
2. Enable the Service with `systemctl enable librespot`
3. Start Service with `systemctl start librespot`
4. 
