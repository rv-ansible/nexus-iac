# nexus-iac
Nexus Infrastructure As Code

### Prerequisites
- centos8 with sudo access
- binaries (if you can't download)
    epel-release
    wget
    nexus-3.62.0-01-unix.tar.gz
    java-1.8.0-openjdk.x86_64
    maven

### Instructions

On <home>/.bashrc add,
```
export ansible_user=xxx
export ansible_password=xxx
```
Make sure ansible_user have sudo access.

Run the ansible in cli,
```
ansible-playbook -i inventory/linux.ini deploy.yml -v
```