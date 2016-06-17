# Ansible Playbook: jeffhung.java-se

Ansible playbook for installing Java SE on CentOS/Debian Linux

## Usage

Install this playbook:

	ansible-galaxy install jeffhung.java-se

Execute this playbook directly:

	ansible-playbook $roles_path/jeffhung.java-se/tasks/install.yml

Or include as a role:

	- hosts: default
	  roles:
		  - jeffhung.java-se

## Role Variables

### `java_variant` (optional)

This playbook could install these Java SE variants:

|           | JRE    | JDK    |
|-----------|--------|--------|
| Java 6 SE | `jre6` | `jdk6` |
| Java 7 SE | `jre7` | `jdk7` |
| Java 8 SE | `jre8` | `jdk8` |

By default `jdk8` will be installed. You could customize which variant to
install by setting the `java_variant` variable:

	- hosts: default
	  roles:
		  - { role: jeffhung.java-se, java_variant: jre7 }

## License

BSD

