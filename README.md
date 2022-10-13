# Set up the ldap-authenticator for leihs

![molecule](https://github.com/elan-ev/leihs_ldap_authenticator/actions/workflows/molecule.yml/badge.svg)

This is an ansible-role to set up the [ldap-authenticator](https://github.com/elan-ev/leihs-ldap-authenticator)
for [leihs](https://github.com/leihs/leihs).

## Role Variables

For a full overview of configuration options look at the [defaults](defaults/main.yml)
and the docs of the [authenticator](https://github.com/elan-ev/leihs-ldap-authenticator#production-deployment).
The default values all-in-all follow the official recommendations from the BigBlueButton docs.
However, you can configure some more options for extra security if you prefer.

## Example Playbook

Your playbook might look like this:

```yaml
---

- hosts: all
  become: true
  roles:
    - role: elan.leihs_ldap_authenticator
```

## Development

For development and testing you can use [molecule](https://molecule.readthedocs.io/en/latest/).
With podman as driver you can install it like this – preferably in a virtual environment:

```bash
pip install -r .dev_requirements.txt
```

Then you can test this role using:

```bash
molecule test
```

## License

[BSD-3-Clause](LICENSE)

## Author Information

[ELAN e.V](https://elan-ev.de/)
