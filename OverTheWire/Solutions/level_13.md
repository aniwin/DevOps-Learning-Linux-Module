# Level 13 Solution

**Level Goal Description**

Goal of this level is to find password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv

## Commands used

1. **Logged into Bandit Level using SSH**

   ```bash
   ssh bandit12@bandit.labs.overthewire.org -p 2220
   ```

2.

**make tmp directory using mktemp -d**

```bash
mktemp -d

```

copy data.txt to temp directory

```bash
cp data.txt /tmp/tmp.aMqrKEkMWQ
```

convert hexdump into binary

```bash
xxd -r data.txt > bandit
```

```bash
file bandit
```

this tell us that it is gzip compressed data, was "data2.bin"

````bash
mv bandit bandit.gz
```

rename file to .gz

```bash
gzip -d bandit.gz
````

decode the file

```bash
file bandit
```

this tell us that it is bzip2 compressed data

```bash
mv databn databn.bz2
```

rename file to .bz2

```bash
bzip2 -d databn.bz2
```

decode using bzip2 command with -d flag

```bash
file databn
```

running file again gives output databn: gzip compressed data, was "data4.bin"

```bash
mv databn databn.gz
```

again rename file to correct file extension

```bash
gzip -d databn.gz
```

decode using gzip -d flag

```bash
file databn
```

I continued to decompress each file depending on its type till eventually got data8: ASCII text back from file command was able to view the password using the cat command

## Password

7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
