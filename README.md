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

java.lang.IllegalArgumentException: Parameter 'credential' may not be null
        at org.wildfly.common.Assert.checkNotNullParamChecked(Assert.java:71)
        at org.wildfly.common.Assert.checkNotNullParam(Assert.java:49)
        at org.wildfly.security.auth.server.ServerAuthenticationContext.addPrivateCredential(ServerAuthenticationContext.java:798)
        at io.quarkus.elytron.security.runtime.ElytronTrustedIdentityProvider$1.get(ElytronTrustedIdentityProvider.java:55)
        at io.quarkus.elytron.security.runtime.ElytronTrustedIdentityProvider$1.get(ElytronTrustedIdentityProvider.java:43)
        at io.quarkus.security.runtime.QuarkusIdentityProviderManagerImpl$1$1$1$1.run(QuarkusIdentityProviderManagerImpl.java:58)
        at io.quarkus.vertx.core.runtime.VertxCoreRecorder$13.runWith(VertxCoreRecorder.java:543)
        at org.jboss.threads.EnhancedQueueExecutor$Task.run(EnhancedQueueExecutor.java:2449)
        at org.jboss.threads.EnhancedQueueExecutor$ThreadBody.run(EnhancedQueueExecutor.java:1478)
        at org.jboss.threads.DelegatingRunnable.run(DelegatingRunnable.java:29)
        at org.jboss.threads.ThreadLocalResettingRunnable.run(ThreadLocalResettingRunnable.java:29)
        at io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
        at java.base/java.lang.Thread.run(Thread.java:832)
