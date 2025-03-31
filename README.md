# Ansible Role: motd

An Ansible Role that configures motd on Ubuntu (for now).

[TOC]

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

### Main Variables

    motd_snippets_custom:
      - 05-custom-uptime-users.sh
      - 07-custom-info.sh
      - 10-custom-help-text.sh

The optional variable `motd_snippets_custom` defines a list of templates for motd scripts which will be copied to the remote host.

    motd_snippets_enabled:
      - 05-custom-uptime-users.sh
      - 07-custom-info.sh
      - 10-custom-help-text.sh

The optional variable `motd_snippets_enabled` defines a list of motd scripts which will be enabled explicitely on the remote host.

    motd_snippets_disabled:
      - 50-motd-news.sh
      - 91-contract-ua-esm-status.sh

The optional variable `motd_snippets_disabled` defines a list of motd scripts which will be disabled explicitely on the remote host.

    motd_infotext: ""

The optional variable `motd_infotext` defines a custom infotext which will be displayed inside the motd on the remote host.

## Dependencies

No dependencies needed.

## Example Playbooks

### Normal usage

    ---
    # This runs the role
    - hosts: localhost
      roles:
        - role:
            name: maxvalue.motd
    ...

## License

[MIT](LICENSE.txt)

## Sponsors

You can support the development of this role and other similar roles by donating to one of the accounts below.

* [bymeacoffee](https://www.buymeacoffee.com/publicbetamax)
* [liberapay](https://de.liberapay.com/maxvalue/)
* [ko-fi](https://ko-fi.com/publicbetamax)
* [Patreon](patreon.com/publicbetamax)

## Author Information

This role was created in 2025 by Max Fuxjäger:
* Mastodon: [@maxvalue@chaos.social](https://chaos.social/@maxvalue)
* Matrix: @ypsilon:matrix.org
