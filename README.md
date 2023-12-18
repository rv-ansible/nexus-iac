# nexus-iac
Nexus Infrastructure As Code

### Prerequisites
- centos8 with sudo access
- internet access
- dns server, if none, use /etc/hosts

_If firewalled, you need these binaries, 
unfortunately you have to do it, 
please add it and create a pull request,_
```
- epel-release
- wget
- nexus-3.62.0-01-unix.tar.gz
- java-1.8.0-openjdk.x86_64
- maven
```

### Instructions

On <home>/.bashrc of ansible, add,
```
export ansible_user=xxx
export ansible_password=xxx
```
Make sure ansible_user have sudo access on the target vm.

Run the ansible in cli,
```
ansible-playbook -i inventory/linux.ini deploy.yml -v
```

***I did not add sudo access on nexus user, it still works, I tested pull on the docker proxy and push on the docker hosted, it works***
