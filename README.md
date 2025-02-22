# Ansible EC2 Instance Management

This project contains an Ansible playbook to manage AWS EC2 instances based on instance tags. It performs the following tasks:

- **Hostname Update**: Sets the instance's hostname based on the **Name** tag.
- **Service Installation**: Installs and configures a service defined in the **Service** tag (e.g., MySQL, Nginx).
- **Version Control**: Ensures the correct service version is installed, based on the **Version** tag.
- **Cron Job for Restart**: Schedules a system restart based on the **Restart** tag, which specifies the day and time.

## Requirements

- Ansible 2.9 or later
- AWS EC2 instances with tags:
  - `Managed: true` (for instances to be managed)
  - `Name`, `Service`, `Version`, and `Restart`

## Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/AviorAtar/Ansible.git
   cd Ansible.git
