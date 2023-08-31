# flatpak

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&amp;logoColor=white)](https://github.com/rolehippie/flatpak)
[![General Workflow](https://github.com/rolehippie/flatpak/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/flatpak/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/flatpak/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/flatpak/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/flatpak/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/flatpak/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/flatpak)](https://github.com/rolehippie/flatpak/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.flatpak-blue)](https://galaxy.ansible.com/rolehippie/flatpak)

Ansible role to install flatpak and configure remotes.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [flatpak_installs_extra](#flatpak_installs_extra)
  - [flatpak_installs_general](#flatpak_installs_general)
  - [flatpak_remotes_extra](#flatpak_remotes_extra)
  - [flatpak_remotes_general](#flatpak_remotes_general)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`


## Default Variables

### flatpak_installs_extra

List of extra packages

#### Default value

```YAML
flatpak_installs_extra: []
```

#### Example usage

```YAML
flatpak_installs_extra:
  - name: net.blix.BlueMail
    state: absent
  - name: io.kinvolk.Headlamp
    method: user
    remote: flathub
    state: present
```

### flatpak_installs_general

List of general packages

#### Default value

```YAML
flatpak_installs_general: []
```

#### Example usage

```YAML
flatpak_installs_general:
  - name: net.blix.BlueMail
    state: absent
  - name: io.kinvolk.Headlamp
    method: user
    remote: flathub
    state: present
```

### flatpak_remotes_extra

List of extra remotes

#### Default value

```YAML
flatpak_remotes_extra: []
```

#### Example usage

```YAML
flatpak_remotes_extra:
  - name: flathub
    url: https://flathub.org/repo/flathub.flatpakrepo
  - name: example
    url: https://example.com/example.flatpakrepo
    method: system
    enabled: True
    state: present
```

### flatpak_remotes_general

List of general remotes

#### Default value

```YAML
flatpak_remotes_general:
  - name: flathub
    url: https://flathub.org/repo/flathub.flatpakrepo
```

#### Example usage

```YAML
flatpak_remotes_general:
  - name: flathub
    url: https://flathub.org/repo/flathub.flatpakrepo
  - name: example
    url: https://example.com/example.flatpakrepo
    method: system
    enabled: True
    state: present
```

## Discovered Tags

**_flatpak_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
