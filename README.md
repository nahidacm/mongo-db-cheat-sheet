#### Enable MongoDB Authentication

1. `vim /etc/mongod.conf`
2. Uncomment the 'security' option and add the configuration as below.
```
security
    authorization: "enabled"
```
`systemctl restart mongod`

#### Login from console
1. `mongo`
2. `use admin`
3. `show users`
4. `db.auth('admin', 'hakasepasswordformongodbadmin')`
5. `show users`
