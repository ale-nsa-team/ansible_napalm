# Ansible & NAPALM Installation

This repository provides a demo environment for using **Ansible** with **NAPALM** to manage Alcatel-Lucent Enterprise OmniSwitch.  
It includes example folders, configuration files, and a Docker-based all-in-one setup.

---

## Prerequisites

- Linux system
- Python **3.x**
- Internet access to install Python packages
- (Optional) Docker
- (Optional) Git

⚠️ **Important:**  
You must have a properly configured DNS **or** manually populate `/etc/hosts` to resolve device names.

---

## Local Installation (Without Docker)

After updating your system and installing Python 3, install the required packages using `pip`.

### Install Python pip
```bash
apt install python3-pip
```

### Install required Python packages
```bash
pip install napalm
pip install ansible
pip install napalm-aos
pip install napalm-ansible
```

---

## Clone the Repository

Clone the repository using Git:

```bash
git clone https://github.com/alenterprise/ansible_napalm.git
cd ansible_napalm
```

### Repository Content

The repository contains:
- Various folders used in the demos
- An Ansible inventory file (`hosts`)
- Example playbooks and network files
- A `Dockerfile` to build a complete demo environment

---

## Docker Installation (Recommended)

### Build the Docker Image

From the directory containing the `Dockerfile`:

```bash
docker build -t whatever/test .
```

### Run the Prebuilt All-in-One Container

A prebuilt container is available on Docker Hub:

```bash
docker run -it --name yourname alenterprise/ansible /bin/bash
```

---

## Docker Environment Details

- **Working directory:** `/home/work`
- Includes:
  - The Git repository
  - The Ansible `hosts` file
  - Demo folders:
    ```bash
    backup  hosts  network  services
    ```

---

## Notes

- The Docker container has been uploaded to **Docker Hub**
- Ensure device hostnames resolve correctly (DNS or `/etc/hosts`)
- This environment is intended for demo and learning purposes
