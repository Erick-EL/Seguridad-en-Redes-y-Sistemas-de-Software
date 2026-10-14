## Descripción 
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [dolls.jpg](https://challenge-files.cylabacademy.net/library/370b91d430bc7ec8382557bcd2fba17a0e4e8ff86df14476a40c9f4b91276fa8/dolls.jpg)
## Solución 
```
└─$ unzip dolls.jpg 
Archive:  dolls.jpg
warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/2_c.jpg     
                                                                                     
┌──(kali㉿kali)-[~/cylab/WebNet0]
└─$ cd base_images  
                                                                                     
┌──(kali㉿kali)-[~/cylab/WebNet0/base_images]
└─$ ls    
2_c.jpg
                                                                                     
┌──(kali㉿kali)-[~/cylab/WebNet0/base_images]
└─$ binwalk dolls.jpg

General Error: Cannot open file dolls.jpg (CWD: /home/kali/cylab/WebNet0/base_images) : [Errno 2] No such file or directory: 'dolls.jpg'

                                                                                     
┌──(kali㉿kali)-[~/cylab/WebNet0/base_images]
└─$ unzip 2_c.jpg  
Archive:  2_c.jpg
warning [2_c.jpg]:  187707 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/3_c.jpg     
                                                                                     
┌──(kali㉿kali)-[~/cylab/WebNet0/base_images]
└─$ cd base_images 
                                                                                     
┌──(kali㉿kali)-[~/cylab/WebNet0/base_images/base_images]
└─$ cd base_images
cd: no such file or directory: base_images
                                                                                     
┌──(kali㉿kali)-[~/cylab/WebNet0/base_images/base_images]
└─$ ls
3_c.jpg
                                                                                     
┌──(kali㉿kali)-[~/cylab/WebNet0/base_images/base_images]
└─$ unzip 3_c.jpg 
Archive:  3_c.jpg
warning [3_c.jpg]:  123606 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/4_c.jpg     
                                                                                     
┌──(kali㉿kali)-[~/cylab/WebNet0/base_images/base_images]
└─$ cd base_images 
                                                                                     
┌──(kali㉿kali)-[~/…/WebNet0/base_images/base_images/base_images]
└─$ unzip 4_c.jpg 
Archive:  4_c.jpg
warning [4_c.jpg]:  79578 extra bytes at beginning or within zipfile
  (attempting to process anyway)
 extracting: flag.txt                
                                                                                     
┌──(kali㉿kali)-[~/…/WebNet0/base_images/base_images/base_images]
└─$ cat flag.txt    
academy{ZNTyvSDXRNO1d0xCkBRMhAoiafpCTvgW}
```
academy{ZNTyvSDXRNO1d0xCkBRMhAoiafpCTvgW}
## Notas adicionales 
- Descomprimir cada zip hasta llegar a la muñeca mas pequeña 
## Referencias