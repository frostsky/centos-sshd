# Pull and Run
```
$ docker pull frostsky/centos-sshd:6.7
$ IMAGENAME=yourimagename
$ docker run -d --name $IMAGENAME frostsky/centos-sshd:6.7
```
# SSH Access
```
$ IP=$(docker inspect -f "{{.NetworkSettings.IPAddress}}" $IMAGENAME)
$ ssh $IP -l root
root@${IP}'s password: frostsky
```
