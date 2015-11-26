# Ansible Role: Symfony 2

An Ansible role that can configure a Symfony 2 application.

## Requirements

For the configuration with nginx the directories for sites must already exist (e.g. nginx has to be installed).
PHP has to be installed for running various tasks (composer, app/console, etc)
Composer has to be installed in PATH as "composer" for running "composer install".

## Role Variables

Available variables are listed below, along with default values:

    symfony2_project_root: /var/www
    symfony2_web_server: nginx
    symfony2_php_fpm_socket: localhost:9000

    symfony2_bash_completion: true

    symfony2_composer_install: true
    symfony2_clear_cache: true

    symfony2_doctrine_schema_update: [] # List of objects with properties "em" and "env"

## Dependencies

None

## Example Playbook

    - hosts: all
      roles:
        - { role: mjanser.symfony2 }

## License

MIT
