# Level 16 Solution

**Level Goal Description**

The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

## Commands used

1. **connected by ssh using password obtained from Level 15**

```bash
 ssh bandit16@bandit.labs.overthewire.org -p 2220
```

## Step 2: Input Current Level Password and Retrieve Next Level Password

1. Connect to the server using OpenSSL to input the current level password:

   ```bash
   openssl s_client --connect localhost:31790 --quiet
   ```

2. Enter the password found in **level 15** when prompted.

3. The server will respond with a **private key** and then close the connection.

4. Create a temporary directory to store the private key securely:

   ```bash
   mktemp -d
   ```

5. Save the private key to a file (replace `PRIVATE KEY HERE` with the actual key you received):

   ```bash
   echo "PRIVATE KEY HERE" > lvl17key.private
   ```

6. Restrict permissions on the private key file:

   ```bash
   chmod 400 lvl17key.private
   ```

7. Use the private key to SSH into the next level:

   ```bash
   ssh -i lvl17key.private bandit17@bandit.labs.overthewire.org -p 2220
   ```

8. Use cat /etc/bandit_pass/bandit17 to get password of bandit17

   ```bash
   ssh -i lvl17key.private bandit17@bandit.labs.overthewire.org -p 2220
   ```

## Password

EReVavePLFHtFlFsjn3hyzMlvSuSAcRD
