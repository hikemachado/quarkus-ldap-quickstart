Quarkus Elytron Security with LDAP Realm
based on
Quarkus Elytron Security with JDBC Realm
========================

This guide demonstrates how your Quarkus application can use a LDAP to store your user identities.

It is using a cloud LDAP to test



## Start the application

The application can be started using: 

```bash
mvn quarkus:dev
```  

## Test the application

in the browser try to access the following URL
* `/api/admin`

you will be redirect to login.html page

use the credential
username: einstein
password:password

the you will face the error
