# ssh2docker

```bash=
docker pull ubuntu:latest
docker run -it --privileged=true -p 50022:22 --name ubuntu ubuntu bash
apt-get update
apt-get install vim	
apt-get install git	
apt-get install net-tools
apt-get install openssh-server
echo "Port 22" >>/etc/ssh/sshd_config
echo "PermitRootLogin yes" >>/etc/ssh/sshd_config
service ssh start	
service ssh status
systemctl enable ssh

echo "#!/bin/bash" >> ssh_auto_start.sh
echo "service ssh start" >> ssh_auto_start.sh
echo "service ssh status" >> ssh_auto_start.sh

chmod 755 ~/ssh_auto_start.sh

echo "~/ssh_auto_start.sh" /root/.bashrc

passwd
```
