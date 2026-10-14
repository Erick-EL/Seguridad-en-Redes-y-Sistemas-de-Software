## Descripción 
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

[Download disk image](https://challenge-files.cylabacademy.net/library/d8718cbbc14dcd9f9aad532a51d7a01b00e1715ca3b1d654dfef687d0b15cbf5/disk.img.gz) Access checker program: `nc xebec.cylabacademy.net 26776`
## Solución 
```
┌──(kali㉿kali)-[~/cylab]
└─$ gzip -d disk.img.gz 
                                                                                     
┌──(kali㉿kali)-[~/cylab]
└─$ nc nc xebec.cylabacademy.net 26776
nc: forward host lookup failed: No address associated with name
                                                                                     
┌──(kali㉿kali)-[~/cylab]
└─$ nc xebec.cylabacademy.net 26776 
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752  
202752
Great work!
academy{mm15_f7w!}
```
## Notas adicionales 
* se uso el gzip -d y file el mmls para ver las particiones
## Referencias