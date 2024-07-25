# Using SSH Jump hosts

In order to gain access to a remote server, you may need to first connect to a jump host. This is a server that is accessible from the internet and can be used to connect to other servers that are not directly accessible from the internet.

To connect to a server via a jump host, you can use the `-J` option with the `ssh` command. For example:

```bash
ssh -J user@jump_host user@target_host
```

This will connect to the `jump_host` first and then connect to the `target_host` from there.

You can also use the `ProxyJump` option in your SSH configuration file to specify a jump host for a particular server. For example:

```bash
# A virtual machine running locally with access to a VPN
Host fedora-vm
  HostName 192.168.122.223
  User <user>

# A server accessible inside of the VPN
Host fedora-server
  HostName 192.168.200.200
  ForwardAgent yes
  User <user>
  ProxyJump fedora-vm
```