# Ansible role: fastfetch

[![Ansible Galaxy downloads](https://img.shields.io/ansible/role/d/Xenion1987/fastfetch?label=Galaxy%20downloads&logo=ansible&color=%23096598)](https://galaxy.ansible.com/ui/standalone/roles/Xenion1987/fastfetch)
[![Ansible Galaxy](https://img.shields.io/badge/role-fastfetch-000000.svg?logo=ansible)](https://galaxy.ansible.com/xenion1987/fastfetch)
[![CI](https://github.com/xenion1987/ansible-role-fastfetch/actions/workflows/ci.yml/badge.svg)](https://github.com/xenion1987/ansible-role-fastfetch/actions/workflows/ci.yml)
[![License](https://img.shields.io/github/license/Xenion1987/ansible-role-fastfetch)](https://github.com/Xenion1987/ansible-role-fastfetch/blob/main/LICENSE)
[![Maintained](https://img.shields.io/badge/Maintained-yes-success.svg)](https://github.com/Xenion1987/ansible-role-fastfetch)
[![Molecule](https://img.shields.io/badge/tested%20with-Molecule-blue.svg)](https://github.com/ansible-community/molecule)

Install the latest `fastfetch` version from GitHub.
Fall back to `fastfetch` version 2.7.1 if the target's
latest version is 'glib<2.35'.

## Table of contents

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [fastfetch_dependencies](#fastfetch_dependencies)
  - [fastfetch_fallback_version](#fastfetch_fallback_version)
  - [fastfetch_force_update](#fastfetch_force_update)
  - [fastfetch_github_orga](#fastfetch_github_orga)
  - [fastfetch_github_repo](#fastfetch_github_repo)
  - [fastfetch_glib_requirement_latest](#fastfetch_glib_requirement_latest)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.11`

## Default Variables

### fastfetch_dependencies

List of dependencies for fastfetch

**_Required:_** True<br />
**_Type:_** dict<br />

#### Default value

```YAML
fastfetch_dependencies:
  deb_based:
    - libc6
  rpm_based:
    - glibc
```

### fastfetch_fallback_version

Fallback fastfetch version if 'glib < fastfetch_glib_requirement_latest'

**_Required:_** True<br />
**_Type:_** string<br />

#### Default value

```YAML
fastfetch_fallback_version: 2.7.1
```

### fastfetch_force_update

Always check and install latest version

**_Required:_** False<br />
**_Type:_** bool<br />

#### Default value

```YAML
fastfetch_force_update: 'false'
```

### fastfetch_github_orga

fastfetch's GitHub repository name

**_Required:_** True<br />
**_Type:_** string<br />

#### Default value

```YAML
fastfetch_github_orga: fastfetch-cli
```

### fastfetch_github_repo

fastfetch's GitHub repository name

**_Required:_** True<br />
**_Type:_** str<br />

#### Default value

```YAML
fastfetch_github_repo: fastfetch
```

### fastfetch_glib_requirement_latest

Min. 'glib' version required for installing 'latest' fastfetch version

**_Required:_** True<br />
**_Type:_** string<br />

#### Default value

```YAML
fastfetch_glib_requirement_latest: '2.35'
```

## Dependencies

None.

## License

BSD, MIT

## Author

[Xenion1987](https://github.com/Xenion1987)
