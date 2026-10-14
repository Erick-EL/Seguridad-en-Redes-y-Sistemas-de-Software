## Descripción 
Download this disk image, find the key and log into the remote machine.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download disk image](https://challenge-files.cylabacademy.net/library/bac64668d6b7caead36e15b7bfc362eeea2c831d367e655a082b9fe63bd85610/disk.img.gz)
- Remote machine: `ssh -i key_file -p 41048 ctf-player@xebec.cylabacademy.net`
## Solución 
```
──(kali㉿kali)-[~/cylab/OperationOni]
└─$ fls -r -o 206848 disk.img | grep -iE "\.ssh|key|id_rsa"
+ d/d 33:       keymap
++ d/d 44:      keys
+++ r/r 907:    cryptkey.files
+++ r/r 922:    keymap.files
++ r/r 554:     save-keymaps
++ r/r 15:      ssh_host_ed25519_key
++ r/r 16:      ssh_host_ed25519_key.pub
++ r/r 17:      ssh_host_ecdsa_key
++ r/r 18:      ssh_host_ecdsa_key.pub
++ r/r 19:      ssh_host_dsa_key
++ r/r 20:      ssh_host_dsa_key.pub
++ r/r 21:      ssh_host_rsa_key
++ r/r 22:      ssh_host_rsa_key.pub
+++++ r/r 1050: keywrap.ko
+++++++ r/r 1202:       hyperv-keyboard.ko
++++++ r/r 1213:        dm-flakey.ko
+++++ d/d 2048: key
++++++ r/r 1691:        af_key.ko
++++++ r/r 1884:        act_tunnel_key.ko
+++++ d/d 2066: keys
++++++ d/d 2067:        encrypted-keys
+++++++ r/r 2068:       encrypted-keys.ko
++ l/l 355:     showkey
++ r/r 2084:    ssh-keygen
++ r/- * 0:     ssh-keyscan
++ r/r 2193:    keytab-lilo
++ r/r 2143:    ssh-keyscan
++ l/l 346:     setkeycodes
+++ d/d 787:    keys
+ r/r 707:      setup-keymap
+ d/d 3916:     .ssh
                                                                                     
┌──(kali㉿kali)-[~/cylab/OperationOni]
└─$ fls -o 206848 disk.img 3916
r/r 2345:       id_ed25519
r/r 2346:       id_ed25519.pub
                                                                                     
┌──(kali㉿kali)-[~/cylab/OperationOni]
└─$ icat -o 206848 disk.img 2345 > key_file
                                                                                     
┌──(kali㉿kali)-[~/cylab/OperationOni]
└─$ chmod 600 key_file
                                                                                     
┌──(kali㉿kali)-[~/cylab/OperationOni]
└─$ ssh -i key_file -p 41048 ctf-player@xebec.cylabacademy.net
The authenticity of host '[xebec.cylabacademy.net]:41048 ([3.14.181.178]:41048)' can't be established.
ED25519 key fingerprint is: SHA256:ZzFWPkrkkhq4v3aMejPdeBM6CxOJEdDfCOqwc0eXgfY
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[xebec.cylabacademy.net]:41048' (ED25519) to the list of known hosts.
Welcome to Ubuntu 24.04.4 LTS (GNU/Linux 7.0.0-1014-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ ls -la
cat flag.txt
total 4
drwxr-xr-x 1 ctf-player ctf-player 20 Oct  8 01:58 .
drwxr-xr-x 1 root       root       24 Sep 23 02:58 ..
drwx------ 2 ctf-player ctf-player 34 Oct  8 01:58 .cache
drwxr-xr-x 2 ctf-player ctf-player 29 Sep 23 02:58 .ssh
-rw-r--r-- 1 root       root       28 Sep 23 02:58 flag.txt
academy{k3y_5l3u7h_127b8b44}ctf-player@challenge:~$ Connection to xebec.cylabacademy.net closed by remote host.
Connection to xebec.cylabacademy.net closed.

```
## Notas adicionales 
* se uso el mmls, fls icat y me concecte por ssh
## Referencias
