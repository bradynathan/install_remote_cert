# README.md
# Ansible Role: install_remote_cert

This role adds a certificate trust to the system it is run on.  An example usage would be adding a self signed certificate to the system.  The SSL certificate hosted on a remote server must include the intermediary certificate that was used to sign itself.

## Requirements

Ansible 2.4

## Role Variables

Available variables are listed below, along with default values:

*  cert_remote_server: www.google.com
*  cert_remote_port: 443


## Dependencies

Requires openssl installed on the target.

## Example Playbook

    - hosts: all
      vars:
        cert_remote_server: satellite.example.local
        cert_remote_port: 443
      roles:
        - install_remote_cert

## License

GPLv3
