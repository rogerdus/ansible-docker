# 🎫 Server Automated Deployment (Ansible)

This repository provides Ansible playbooks to automate the end-to-end installation. By leveraging Docker, these playbooks ensure a consistent, reproducible, and isolated environment.
📋 Table of Contents

    Features

    Prerequisites

    Quick Start

    Configuration

✨ Features

    Automated Docker Setup: Installs Docker and Docker Compose on the target machine.

    Dependency Management: Handles all PHP extensions and web server requirements via containers.

    Idempotency: Safe to run multiple times without breaking existing configurations.

💻 Prerequisites

Before running the playbooks, ensure you have:

    Control Node: Ansible 2.15+ installed.

    Managed Node: A Linux server (Ubuntu/Debian recommended) with SSH access.

    Privileges: sudo access on the target host.

🚀 Quick Start

Follow these steps to get your instance up and running:
1. Prepare the Inventory

Copy the example inventory file and update it with your server's IP and SSH credentials:
Bash

cp inventory.example.ini inventory.ini
# Edit the file with your favorite editor
nano inventory.ini

2. Run the Playbook

Execute the following command to start the installation process:
Bash

ansible-playbook -i inventory.ini install_docker.yml

⚙️ Configuration
Variable	Default	Description
docker_compose_version	latest	Version of Docker Compose to install.
