# easyrsa-web-ui

It's web ui for easyrsa. Written by GO.

Optionary supported to output openvpn client configuration file.

# how to use

```bash
git clone https://github.com/okayasu/easyrsa-web-ui
cd easyrsa-web-ui
cp config.toml.sample config.toml
[edit config.toml]
go run main.go init
go run main.go
```

`go run main.go init` command may download easyrsa and build pki folder. It's failed when pki distination folder exist. So easy way is to make pki on tempolary folder and move it.

Not support Authorization. Easyrsa-web-ui is designed to use under reverse proxy. 

## configurations

* [easyrsa.path] easyrsa install folder
* [easyrsa.pki_path] build and use pki folder
* [http.port] lisetne port
* [http.host] lisetne interface
* [openvpn.support] enable ovpn file configure and output
* [openvpn.client_config] template configure to openvpn client