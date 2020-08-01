# Bandit Level 12 → Level 13

**Hostname:** bandit.labs.overthewire.org

**Username:** bandit12

**Password:** 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu

```
ssh -p 2220 bandit12@bandit.labs.overthewire.org
```

## Level Goal

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Commands Used

ls - list directory contents

cd - change directory

mkdir - make directories

cp - copy files and directories

mv - move (rename) files

xxd - make a hexdump or do the reverse
- **-r | -revert** Reverse operation: convert (or patch) hexdump into binary

gzip - compress or expand files
- **-d --decompress --uncompress** Decompress

bzip2, bunzip2 - a block-sorting file compressor
- **-d --decompress** Force decompression

tar - an archiving utility
- **-x, --extract, --get** Extract files from an archive
- **-f, --file=ARCHIVE** Use archive file or device ARCHIVE
- **-v, --verbose** Verbosely list files processed

## Solution

```
bandit12@bandit:~$ ls
data.txt
```
```
bandit12@bandit:~$ mkdir /tmp/mwalrath
```
```
bandit12@bandit:~$ cp data.txt /tmp/mwalrath/
```
```
bandit12@bandit:~$ cd /tmp/mwalrath
```
```
bandit12@bandit:/tmp/mwalrath$ xxd -r data.txt data
```
```
bandit12@bandit:/tmp/mwalrath$ file data
data: gzip compressed data, was "data2.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix
```
```
bandit12@bandit:/tmp/mwalrath$ mv data data.gz
```
```
bandit12@bandit:/tmp/mwalrath$ gzip -d data.gz
```
```
bandit12@bandit:/tmp/mwalrath$ file data
data:    bzip2 compressed data, block size = 900k
```
```
bandit12@bandit:/tmp/mwalrath$ mv data data.bz2
```
```
bandit12@bandit:/tmp/mwalrath$ bzip2 -d data.bz2
```
```
bandit12@bandit:/tmp/mwalrath$ file data
data: gzip compressed data, was "data4.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix
```
```
bandit12@bandit:/tmp/mwalrath$ mv data data.gz
```
```
bandit12@bandit:/tmp/mwalrath$ gzip -d data.gz
```
```
bandit12@bandit:/tmp/mwalrath$ file data
data:    POSIX tar archive (GNU)
```
```
bandit12@bandit:/tmp/mwalrath$ tar -xvf data
data5.bin
```
```
bandit12@bandit:/tmp/mwalrath$ file data5.bin
data5.bin: POSIX tar archive (GNU)
```
```
bandit12@bandit:/tmp/mwalrath$ tar -xvf data5.bin
data6.bin
```
```
bandit12@bandit:/tmp/mwalrath$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
```
```
bandit12@bandit:/tmp/mwalrath$ mv data6.bin data6.bz2
```
```
bandit12@bandit:/tmp/mwalrath$ bzip2 -d data6.bz2
```
```
bandit12@bandit:/tmp/mwalrath$ file data6
data6: POSIX tar archive (GNU)
```
```
bandit12@bandit:/tmp/mwalrath$ tar -xvf data6
data8.bin
```
```
bandit12@bandit:/tmp/mwalrath$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix
```
```
bandit12@bandit:/tmp/mwalrath$ mv data8.bin data8.gz
```
```
bandit12@bandit:/tmp/mwalrath$ gzip -d data8.gz
```
```
bandit12@bandit:/tmp/mwalrath$ file data8
data8: ASCII text
```
```
bandit12@bandit:/tmp/mwalrath$ cat data8
The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
```
