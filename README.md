#### Enable MongoDB Authentication

1. `vim /etc/mongod.conf`
2. Uncomment the 'security' option and add the configuration as below.
```
security
    authorization: "enabled"
```
`systemctl restart mongod`

#### Login from console
1. `mongosh`
2. `use admin`
3. `show users`
4. `db.auth('admin', 'hakasepasswordformongodbadmin')`
5. `show users`

#### Create user
`use <db name>`
````javascript
db.createUser(
   {
     user: "username",
     pwd: passwordPrompt(),  // Or  "<cleartext password>"
     roles: [ "readWrite", "dbAdmin" ]
   }
)
````

#### CRUD

https://developer.mongodb.com/quickstart/cheat-sheet/
