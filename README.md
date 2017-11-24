![Logo](https://raw.githubusercontent.com/idealista/nodejs-role/master/logo.gif)

[![Build Status](https://travis-ci.org/idealista/nodejs-role.svg?branch=master)](https://travis-ci.org/idealista/nodejs-role)
# Node.js Ansible role

This ansible role installs Node.js runtime in a debian environment.

- [Getting Started](#getting-started)
	- [Prerequisities](#prerequisities)
	- [Installing](#installing)
- [Usage](#usage)
- [Testing](#testing)
- [Built With](#built-with)
- [Versioning](#versioning)
- [Authors](#authors)
- [License](#license)
- [Contributing](#contributing)

## Getting Started

These instructions will get you a copy of the role for your ansible playbook. Once launched, it will install a [nodejs](https://nodejs.org/) JavaScript runtime.

### Prerequisities

Ansible 2.3.1.0 version installed.
Inventory destination should be a Debian environment.

For testing purposes, [Molecule](https://molecule.readthedocs.io/) with [Docker](https://www.docker.com/) and [Vagrant](https://www.vagrantup.com/) as driver (with [landrush](https://github.com/vagrant-landrush/landrush) plugin) and [VirtualBox](https://www.virtualbox.org/) as provider.

### Installing

Create or add to your roles dependency file (e.g requirements.yml):

```
- src: idealista.nodejs-role
  version: 1.0.0
  name: nodejs
```

Install the role with ansible-galaxy command:

```
ansible-galaxy install -p roles -r requirements.yml -f
```

Use in a playbook:

```
- hosts: someserver
  roles:
    - role: nodejs
```

## Usage

Look to the [defaults](defaults/main.yml) properties file to see the possible configuration properties.

Default version always is LTS. Feel free to choose another version if you prefer.

## Testing

```sh
molecule test
```

## Built With

![Ansible](https://img.shields.io/badge/ansible-2.3.1.0-green.svg)

![Molecule](https://img.shields.io/badge/molecule-1.25.0-green.svg)

![Goss](https://img.shields.io/badge/goss-0.3.5-green.svg)


## Versioning

For the versions available, see the [tags on this repository](https://github.com/idealista/nodejs-role/tags).

Additionaly you can see what change in each version in the [CHANGELOG.md](CHANGELOG.md) file.

## Authors

* **Idealista** - *Work with* - [idealista](https://github.com/idealista)

See also the list of [contributors](https://github.com/idealista/nodejs-role/contributors) who participated in this project.

## License

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

This project is licensed under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) license - see the [LICENSE](LICENSE.txt) file for details.

## Contributing

Please read [CONTRIBUTING.md](.github/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.
