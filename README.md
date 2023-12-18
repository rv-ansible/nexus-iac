# nexus-iac
Nexus Infrastructure As Code

### Prerequisites
- centos8 with sudo access
- internet access
- dns server, if none, use /etc/hosts

### if firewalled, you need these binaries, 
### unfortunately you have to do it, 
### please add it and create a pull request,
```
- epel-release</br>
- wget</br>
- nexus-3.62.0-01-unix.tar.gz</br>
- java-1.8.0-openjdk.x86_64</br>
- maven</br>
```

### Instructions

On <home>/.bashrc of ansible, add,
```
export ansible_user=xxx
export ansible_password=xxx
```
Make sure ansible_user have sudo access.

Run the ansible in cli,
```
ansible-playbook -i inventory/linux.ini deploy.yml -v
```
