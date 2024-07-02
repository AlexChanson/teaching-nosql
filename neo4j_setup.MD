## Setup DBMS
Configure repo 
```
rpm --import https://debian.neo4j.com/neotechnology.gpg.key
cat << EOF >  /etc/yum.repos.d/neo4j.repo
[neo4j]
name=Neo4j RPM Repository
baseurl=https://yum.neo4j.com/stable/5
enabled=1
gpgcheck=1
EOF
```
Install package
`yum install neo4j-5.21.0`

### Set an initial password
`neo4j-admin dbms set-initial-password student2024`

### Pin and start service
```
systemctl enable neo4j
systemctl start neo4j
```

## First steps
### Connect
The query tool is integrated into the server [http://localhost:7474/browser](http://localhost:7474/browser)
### User/password
neo4j/student2024

## Sources
Official documentation linux install [https://neo4j.com/docs/operations-manual/current/installation/linux/rpm/#linux-rpm-install](https://neo4j.com/docs/operations-manual/current/installation/linux/rpm/#linux-rpm-install)
