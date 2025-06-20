# Level 15 Solution

**Level Goal Description**

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

## Commands used

1. **connected by creating an SSL/TLS client connection with openssl s_client on localhost at port 30001**

```bash
openssl s_client -crlf \
-connect localhost:30001 \
-servername localhost
```

2. **input current level password in, program returns correct! and password for next level**

## Password

kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
