All about the Linux Setup

```bash
sudo ufw allow from 192.168.0.0/24 to any proto tcp

sudo ufw allow from 192.168.1.0/24 to any proto tcp


sudo ufw allow from 127.0.0.1 to any proto tcp

sudo ufw status
```


If you want to remove the rules
```bash
sudo ufw delete allow ssh
sudo ufw delete allow from 192.168.1.2 to any port ssh
sudo ufw delete allow from 127.0.0.1 to any port 22 proto tcp
sudo ufw delete allow from 192.168.0.0/24 to any port ssh
```


Some things you need to do if ssh client still doesn't work

```
   # Remove SSH with the following command:
    sudo apt-get remove openssh-client openssh-server

   # Install SSH again with:
    sudo apt-get install openssh-client openssh-server

```
