# Ansible Nginx Deployment Role

This Ansible role installs and configures Nginx and deploys a simple web page.

The role is designed to be reusable. Application name, environment, and message can be customized through variables.

## Requirements

- Ansible 2.16 or later
- Ubuntu/Debian-based target server
- SSH access to the target server
- `become: true` permission for installing Nginx

## Role Variables

The following variables are available in `defaults/main.yml`:

| Variable | Default Value | Description |
|---|---|---|
| `app_name` | `Ansible Role Demo` | Application name displayed on the web page |
| `app_environment` | `POC Environment` | Environment name displayed on the web page |
| `app_message` | `This page is deployed using Ansible.` | Message displayed on the web page |

These values can be overridden from the playbook.

## What This Role Does

The role performs the following tasks:

1. Installs Nginx.
2. Deploys the HTML page using an Ansible template.
3. Deploys the CSS file.
4. Starts Nginx.
5. Enables Nginx to start automatically after reboot.

## Dependencies

No other Ansible roles are required.

## Installation

Install the role from Ansible Galaxy:

```bash
ansible-galaxy role install <galaxy-username>.<role-name>
