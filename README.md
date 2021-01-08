# motd

This role will create a motd banner when logging into your server.

## Example

```yaml
---

- host: all
  roles:
    - totaldebug/motd
```

This playbook produces the `/etc/motd' file looking like this:

```shell
[root@localhost ~]# cat /etc/motd
     _              _ _     _
    / \   _ __  ___(_) |__ | | ___
   / _ \ | '_ \/ __| | '_ \| |/ _ \
  / ___ \| | | \__ \ | |_) | |  __/
 /_/   \_\_| |_|___/_|_.__/|_|\___|

 FQDN:    localhost.localdomain - WebServer
 Distro:  CentOS 7.7 Final
 Last Change: 2019-12-18, 16:41:04
 CPUs:    1
 RAM:     0.49GB

```

## Role variables

- `motd_template`: modify this to change the ASCII Art or possible options
- `motd_modification`: should the motd be modified defaults `true`
- `motd_server_role`: What role the server plays e.g. `WebServer`
- `motd_info`: List of additional information to show under the ASCII art. Look
into the `defaults` for an example.

## Custom Templates

The templates packaged with this role are meant to be very generic.

If the default template does not suit your needs, you can replace it with yours. What you need to do:

create a templates directory at the same level as your playbook
create a `templates\mymotd.j2` file (just choose a different name from the default template)
in your playbook set the var `motd_template: mymotd.j2`

## License

MIT
