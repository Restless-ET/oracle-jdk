Ansible Java Oracle JDK Role
======

[![Build Status](https://travis-ci.org/fabiohbarbosa/ansible-java-jdk-role.png)](https://travis-ci.org/fabiohbarbosa/ansible-java-jdk-role)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-docker-blue.svg?style=flat-square)](https://galaxy.ansible.com/fabiohbarbosa/oracle-java-jdk/)
[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)


Ansible role to install the latest update of Oracle/Sun JDK version(s).


Forked: [ANXS.oracle-jdk](https://github.com/ANXS/oracle-jdk). Motivation: keep the ansible role up to date and making improvements.


#### Requirements & Dependencies
- Tested on Ansible 2.0


#### Variables

```yaml
oracle_jdk_java_versions: [8]             # A list of java versions you want to have installed (6, 7, 8 and/or 9)
oracle_jdk_java_version_default: 8        # The java version you want to be the system default
```


#### In operation

To switch between different Java versions, you could use the following terminal command:
```bash
sudo update-alternatives --config java
```


#### Example Playbook

See [galaxy role](https://galaxy.ansible.com/fabiohbarbosa/oracle-java-jdk/)

```yaml
  roles:
    - { role: fabiohbarbosa.oracle-java-jdk, oracle_jdk_java_versions: [6,7,8,9], oracle_jdk_java_version_default: 8 }
```


#### Testing
This project comes with a VagrantFile, this is a fast and easy way to test changes to the role, fire it up with `vagrant up`

See [vagrant docs](https://docs.vagrantup.com/v2/) for getting setup with vagrant


#### License

Licensed under the MIT License. See the LICENSE file for details.


#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/fabiohbarbosa/ansible-java-jdk-role/issues)!
