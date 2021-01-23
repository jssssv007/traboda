***snow snow***:
```
For this question we will be using stegsnow as it contains whitespaces and name of 
this question even suggests the same :) and when we copy the text ; we will get
some whitespaces . Stegsnow basically conceals the message by appending tabs
and spaces at the end of the lines .
"ntio{eP1B35x4K3_aB3O0_q5_K00t}" this is the thing which we get after using stegsnow .
If we observe it according to flag pattern ; we have to go back for 8 steps for 
each alphabet(only alphabets) . Then we will get "flag{wH1T35p4C3_sT3G0_i5_C00l}"
```

***10111001***:
```
In the question ; they have mentioned about significant bytes . So we can use zsteg .
Using this we will get a base 32 encrypted text . 
"NFXGG5DGNJ5TI3K7ORUDGX2MGNAVG5C7GVUUO3RRMYYWGNDOKRPWEVKUL4YV6YZUJZPXI4RQOVBEYM27LEYHKXZUL5WDAVD5"
And the decrypted message is "inctfj{4m_th3_L3ASt_5iGn1f1c4nT_bUT_1_c4N_tr0uBL3_Y0u_4_l0T}"
```

***Detailed view***:
```
For this question ; if we check the metadata of the png file given ; using exiftool ; we will get
a link and if we check the link ; we will see a string which was encode in base64 .
"ZmxhZ3tNMTVzSTBOX2FDYzBNUEwxNWgzRH0=" and the flag is " flag{M15sI0N_aCc0MPL15h3D}".
```

***con-the-cat***:
```
After checking with pngcheck ; we will get an error like we are having additional chunks after IEND.
So if we use binwalk ; we can see that the image is stored using four JPEG files . Now we need to 
use dd tool and we will get the flag as "inctfj{y0u_c4nt_s33_m3!!}" .
```

***back to San Andreas***:
```
In the description ; they have given a hint that we can do this question using JSTEG .(as the letters
j,s,t,e,g were in capital)So using jsteg reveal filename.png x.txt; we will get a url and in that url ;
we can see the flag "inctfj{gr0ve_5treet_f0r_l1fe}".(Inside the image).
```

***always has been***
```
I have downloaded the image and opened it in my image viewer and it seemed to be with grids .
So I have tried it in stegsolve and got the flag " inctfj{the3_fl4g_wa5_liter4lly_ins1de_4_m3m3}".
```

***Jay-chot***:
```
This jpg file shows an error if we try to open it . If we ghex the file ; we can see that some hex
values were not correct (magic number) . If we correct them ; we will get the flag .
"flag{a4aa04741a8d3a952a7ec88457991b97}"
```

***My-First-Stegnography***
```
This question could be solved using "steghide" as it is the tool which will be used for hiding and 
extracting messages inside an image .If we extract the data from the first image using 
steghide "extract -sf forensics-81.jpg" ; we will get the passphrase for the second image and
after extracting from the second image ; we will get the flag ."inctfj{w3_4r3_pl4nt1ng_4_b0mb}".
```

***You Can't See Me***
```
We have to check the png image with "pngcheck" . It will let us know the errors in the hex values 
and we have to corect them . The errors will be as follows:
magic number , IHDR , gAMA , IDAT , IEND .
After correcting them ; we will get the flag ."inctfj{WH4t_ar3_pNgCHUnks?}".
```
***Security 101***
```
Firstly we have to unzip the given file . We have an image "myinspiration"
and we have to check for the username in it .In the question ; they have 
mentioned that username and password could be same .So we have to find the
username . It can be achieved by using exiftool and the username will be in 
the metadata of the image file .And now I know the password and we can unlock 
the zip file to get the image . The image contains the flag .
" inctfj{1ts_4ll_f1ne_tru5t_m3}"
```

***The Office Trouble 1***
```
We can clearly see that it is a zip file which was secured with password . 
To crack it ; we can use fcrackzip . We can proceed in bruteforce method but it
may not be that fast . So we can use the file "rockit.txt" and we can get the 
flag using dictionary method .
"flag = inctfj{dw1ght_1s_cr4zy_bu7_awes0me}"
```



















