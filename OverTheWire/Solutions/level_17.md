# Level 17 Solution

**Level Goal Description**

Level 17 Credentials retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Commands used

Scan ports on localhost to find active services

```bash
nmap -sV localhost -p 31000-32000
```

output

PORT STATE SERVICE VERSION
31046/tcp open echo
31518/tcp open ssl/echo
31691/tcp open echo
31790/tcp open ssl/unknown
31960/tcp open echo

Only port 31790 and 31518/tcp have ssl in service column.

Then found password of level 16 needed for when connecting to correct port.

```bash
cat /etc/bandit_pass/bandit16
```

output: kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

Then tried out to connect to both 31518 and 31790 using openssl. 31518 just printed out what was entered so tried 31790.

```bash
openssl s_client --connect localhost:31790 -quiet
```

Use -quiet to silence keyudate when connecting

This returned an RSA Private key which needed to be saved.

```bash
mktemp -d
```

Save the private key to a file (replace `PRIVATE KEY HERE` with the actual key):

```bash
echo "PRIVATE KEY HERE" > lvl17key.pem
```

Restrict permissions on the private key file:

```bash
chmod 400 lvl17key.pem
```

Use the private key to SSH into the next level:

```bash
ssh -i lvl17key.pem bandit17@bandit.labs.overthewire.org -p 2220
```

Use cat /etc/bandit_pass/bandit17 to get password of bandit17

```bash
cat /etc/bandit_pass/bandit17
```

## Password

EReVavePLFHtFlFsjn3hyzMlvSuSAcRD
