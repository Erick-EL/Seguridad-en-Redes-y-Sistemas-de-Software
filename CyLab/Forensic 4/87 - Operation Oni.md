## Descripción 
Download this disk image and find the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://challenge-files.cylabacademy.net/library/c43b9c25ad2c97fb0c7c393a7b5f95065b79c0faf5848e1eeb6a453ec3e78f7d/disk.flag.img.gz)
## Solución 
```
└─$ fls -0 411648 disk.flag.img -r | grep flag -A 2 -b 2
grep: 2: No such file or directory
fls: invalid option -- '0'
Invalid argument: 411648
usage: fls [-adDFlhpruvV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-m dir/] [-o imgoffset] [-z ZONE] [-s seconds] image [images] [inode]
        If [inode] is not given, the root directory is used
        -a: Display "." and ".." entries
        -d: Display deleted entries only
        -D: Display only directories
        -F: Display only files
        -l: Display long version (like ls -l)
        -i imgtype: Format of image file (use '-i list' for supported types)
        -b dev_sector_size: The size (in bytes) of the device sectors
        -f fstype: File system type (use '-f list' for supported types)
        -m: Display output in mactime input format with
              dir/ as the actual mount point of the image
        -h: Include MD5 checksum hash in mactime output
        -o imgoffset: Offset into image file (in sectors)
        -P pooltype: Pool container type (use '-P list' for supported types)
        -B pool_volume_block: Starting block (for pool volumes only)
        -S snap_id: Snapshot ID (for APFS only)
        -p: Display full path for each file
        -r: Recurse on directory entries
        -u: Display undeleted entries only
        -v: verbose output to stderr
        -V: Print version
        -z: Time zone of original machine (i.e. EST5EDT or GMT) (only useful with -l)
        -s seconds: Time skew of original machine (in seconds) (only useful with -l & -m)
        -k password: Decryption password for encrypted volumes
                                                                                     
┌──(kali㉿kali)-[~/cylab/Operation]
└─$ mmls disk.flag.img                                  
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)
                                                                                     
┌──(kali㉿kali)-[~/cylab/Operation]
└─$ fls -o 411648 disk.flag.img -r | grep flag -A 2 -b 2
grep: 2: No such file or directory
                                                                                     
┌──(kali㉿kali)-[~/cylab/Operation]
└─$ cat -o 411648 disk.flag.img 1782
cat: invalid option -- 'o'
Try 'cat --help' for more information.
                                                                                     
┌──(kali㉿kali)-[~/cylab/Operation]
└─$ cat -O 411648 disk.flag.img 1782
cat: invalid option -- 'O'
Try 'cat --help' for more information.
                                                                                     
┌──(kali㉿kali)-[~/cylab/Operation]
└─$ icat -o 411648 disk.flag.img 1782
Salted__�v �S>�!�jfo(�s:��Kr�ـd�I/Uq�+����fȤ7� ���؎$�'%                                                                                     
┌──(kali㉿kali)-[~/cylab/Operation]
└─$ icat -o 411648 disk.flag.img 1875
touch flag.txt
nano flag.txt 
apk get nano
apk --help
apk add nano
nano flag.txt 
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
                                                                                     
┌──(kali㉿kali)-[~/cylab/Operation]
└─$ openssl aes256 -salt -in flag.txt.enc -out flag.txt -k unbreakablepassword123456 -d
Can't open "flag.txt.enc" for reading, No such file or directory
8067E9B4767F0000:error:80000002:system library:BIO_new_file:No such file or directory:../crypto/bio/bss_file.c:67:calling fopen(flag.txt.enc, rb)
8067E9B4767F0000:error:10000080:BIO routines:BIO_new_file:no such file:../crypto/bio/bss_file.c:75:
                                                                                     
┌──(kali㉿kali)-[~/cylab/Operation]
└─$ icat -o 411648 disk.flag.img 1782 > flag.txt.enc
                                                                                     
┌──(kali㉿kali)-[~/cylab/Operation]
└─$ openssl aes256 -salt -in flag.txt.enc -out flag.txt -k unbreakablepassword123456 -d
academy{h4un71ng_p457_0cf3a06d}
```
## Notas adicionales 
* Todo bien hasta que llego a esta esta parte en este comando y no me deja avanzar no c si es por la palabra unbreakablepassword1234567 que creo que si openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567*
## Referencias
