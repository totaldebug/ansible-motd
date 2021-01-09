<h4 align="center">An Ansible role for creating an MOTD banner when logging into yout server.</h4>

<p align="center">
    <a href="https://github.com/totaldebug/ansible-role-motd/commits/master">
    <img src="https://img.shields.io/github/last-commit/totaldebug/ansible-role-motd.svg?style=flat-square&logo=github&logoColor=white"
         alt="GitHub last commit">
    <a href="https://github.com/totaldebug/ansible-role-motd/issues">
    <img src="https://img.shields.io/github/issues-raw/totaldebug/ansible-role-motd.svg?style=flat-square&logo=github&logoColor=white"
         alt="GitHub issues">
    <a href="https://github.com/totaldebug/ansible-role-motd/pulls">
    <img src="https://img.shields.io/github/issues-pr-raw/totaldebug/ansible-role-motd.svg?style=flat-square&logo=github&logoColor=white"
         alt="GitHub pull requests">
</p>

<p align="center">
  <a href="#configuration">Configuration</a> •
  <a href="#features">Features</a> •
  <a href="#contributing">Contributing</a> •
  <a href="#author">Author</a> •
  <a href="#support">Support</a> •
  <a href="#donate">Donate</a> •
  <a href="#license">License</a>
</p>

---

## Configuration

### Role Variables

- `motd_template`: modify this to change the ASCII Art or possible options
- `motd_modification`: should the motd be modified defaults `true`
- `motd_server_role`: What role the server plays e.g. `WebServer`
- `motd_info`: List of additional information to show under the ASCII art. Look
into the `defaults` for an example.

### Custom Template

The templates packaged with this role are meant to be very generic.

If the default template does not suit your needs, you can replace it with yours. What you need to do:

create a templates directory at the same level as your playbook
create a `templates\mymotd.j2` file (just choose a different name from the default template)
in your playbook set the var `motd_template: mymotd.j2`

### Example Playbook

```yaml
---

- host: all
  roles:
    - totaldebug/motd
```

## Features

|                            |         🔰         |
| -------------------------- | :----------------: |
| Custom Template            |         ✔️         |
| Server information         |         ✔️         |

## Example Output

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

## Contributing

Got **something interesting** you'd like to **share**? Learn about [contributing](https://github.com/totaldebug/.github/blob/main/.github/CONTRIBUTING.md).

## Author

| [![TotalDebug](https://totaldebug.uk/assets/images/logo.png)](https://linkedin.com/in/marksie1988) 	|
|:---------------------------------------------------------------------------------------------------------:	|
|                                            **marksie1988 (Steven Marks)**                                            	|

## Support

Reach out to me at one of the following places:

- via [Discord](https://discord.gg/6fmekudc8Q)
- Raise an issue in GitHub

## Donate


## License

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-orange.svg?style=flat-square)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

- Copyright © [Total Debug](https://totaldebug.uk "Total Debug").
