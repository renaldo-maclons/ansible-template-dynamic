# Ansible Template

My base Ansible template, a good start to deploy to a dynamic host environment where inventories change on the fly, creating roles is outside the scope of this template.

## Getting Started

It's a good place too start  when writing Ansible roles that need to expand dynamically.

### Usage:
```
ansible-playbook -i 'localhost,' ./play.yml -e "ROLE=<role>" -e "TARGET=<n.n.n.n|host@fqdn>" -e "USER=$USER"
```

#### Breakdown:

* **ansible-playbook** -- The CLI command invoking ansible to run a specific playbook **"play.yml"**
* **-i 'localhost,'** -- Our ansible host inventory specification from where the playbook will be executed.
* **-e "VAR=$VAR"** -- Variables handled during runtime of the playbook either passed via a terminal command or any CICD tool such as Jenkins etc.
* Please note the **TARGET** variable is extremely important, this specifies the target machine to be configured by our playbook.

### Prerequisites

What do you need?

```
Any operating system that supports:
Git
Ansible
```

## Built With

* [Ansible](https://www.ansible.com/) - The automation tool used
* [Vagrant](https://www.vagrantup.com/) - Portable virtual software maintainer
* [Virtualbox](https://www.virtualbox.org/wiki/VirtualBox) -  General-purpose full virtualizer for x86 hardware

## Contributing

Please read [CONTRIBUTING.md](https://github.com/rnjudas) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags).

## Authors

* **Renaldo Maclons** - *Initial work* - [RNJudas](https://github.com/rnjudas)

See also the list of [contributors](https://github.com/rnjudas) who participated in this project.

## License

This project is licensed under the MIT License - see the **LICENSE.md** file for details

## Acknowledgments

* Anyone who ever used ansible/vagrant/Linux
