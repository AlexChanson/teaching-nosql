### Setup repo 
Create a config file `/etc/yum.repos.d/mongodb-org-7.0.repo` :
```
[mongodb-org-7.0]
name=MongoDB Repository
baseurl=https://repo.mongodb.org/yum/redhat/9/mongodb-org/7.0/x86_64/
gpgcheck=1
enabled=1
gpgkey=https://pgp.mongodb.com/server-7.0.asc
```

### Install
```
sudo yum update
sudo yum install -y mongodb-org
```

### Config adjustements
Add a line to `/etc/sysctl.conf` :
```
vm.max_map_count=262144 
```


## Sources
Official doc install guide : [https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-red-hat/](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-red-hat/)
