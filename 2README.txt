ZIUA 2 - 17.06.2022

Toate comenzile sunt date dupa ce m-am mutat in directorul Downloads
georgiana@georgiana:~$ cd Downloads


1. Magikarp Ground Mission - picoCTF{xxsh_0ut_0f_\/\/4t3r_5190b070}


georgiana@georgiana:~$ ssh ctf-player@venus.picoctf.net -p 50482
The authenticity of host '[venus.picoctf.net]:50482 ([3.131.124.143]:50482)' can't be established.
ECDSA key fingerprint is SHA256:NrQkIxNEQQho/GA7jE0WlIa7Jh4VF9sAvC5awkbuj1Q.
Are you sure you want to continue connecting (yes/no/[fingerprint])? y
Please type 'yes', 'no' or the fingerprint: yes
Warning: Permanently added '[venus.picoctf.net]:50482,[3.131.124.143]:50482' (ECDSA) to the list of known hosts.
ctf-player@venus.picoctf.net's password: 
Welcome to Ubuntu 18.04.5 LTS (GNU/Linux 5.4.0-1041-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt 
picoCTF{xxsh_
ctf-player@pico-chall$ cat instructions-to-2of3.txt 
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ cd
ctf-player@pico-chall$ ls -a
.  ..  .cache  .profile  .ssh  3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt 
5190b070}
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls -a
.	       bin   home		       media  root  sys
..	       boot  instructions-to-3of3.txt  mnt    run   tmp
.dockerenv     dev   lib		       opt    sbin  usr
2of3.flag.txt  etc   lib64		       proc   srv   var
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_\/\/4t3r_
ctf-player@pico-chall$ Connection to venus.picoctf.net closed by remote host.
Connection to venus.picoctf.net closed.


2. Nice netcat... - picoCTF{g00d_k1tty!_n1c3_k1tty!_7c0821f5}
A trebuit sa transform din zecimal in caracter, foolosind tabela ASCII

georgiana@georgiana:~$ nc mercury.picoctf.net 43239
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
55 
99 
48 
56 
50 
49 
102 
53 
125 
10


3. what's a net cat? - picoCTF{nEtCat_Mast3ry_284be8f7}

georgiana@georgiana:~$ nc jupiter.challenges.picoctf.org 64287
You're on your way to becoming the net cat master
picoCTF{nEtCat_Mast3ry_284be8f7}


4. Glitch Cat - picoCTF{gl17ch_m3_n07_a4392d2e}

georgiana@georgiana:~$ nc saturn.picoctf.net 53933
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'


5. HashingJobApp - picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}

georgiana@georgiana:~$ nc saturn.picoctf.net 63116
Please md5 hash the text between quotes, excluding the quotes: 'Andy Warhol'
Answer: 
024e803352db3cd645a396423ac12c31
024e803352db3cd645a396423ac12c31
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Michelangelo'
Answer: 
0d46a3ff4160862bb8329524b99da972
0d46a3ff4160862bb8329524b99da972
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'a car crash'
Answer: 
55067b2a1b8b8110a7411ba64e6f6168
55067b2a1b8b8110a7411ba64e6f6168
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}


6. runme.py - picoCTF{run_s4n1ty_run}

georgiana@georgiana:~/Downloads$ python3 runme.py
picoCTF{run_s4n1ty_run}


7. Serpentine - picoCTF{7h3_r04d_l355_7r4v3l3d_aa2340b2}
A trebuit sa modific print-ul pentru varianta b. In loc de un mesaj standard, sa imi printeze flag ul.

georgiana@georgiana:~/Downloads$ python3 serpentine.py

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) a

-----------------------------------------------------
Look how far you've come!
-----------------------------------------------------


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b

Oops! I must have misplaced the print_flag function! Check my source code!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) c
georgiana@georgiana:~/Downloads$ gedit serpentine.py &
[1] 5681
georgiana@georgiana:~/Downloads$ python3 serpentine.py

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_aa2340b2}


8. First Find - picoCTF{f1nd_15_f457_ab443fd1}

georgiana@georgiana:~/Downloads$ cd files
georgiana@georgiana:~/Downloads/files$ ls -Ra
.:
.  ..  13771.txt.utf-8  14789.txt.utf-8  acceptable_books  adequate_books  satisfactory_books

./acceptable_books:
.  ..  17879.txt.utf-8  17880.txt.utf-8  more_books

./acceptable_books/more_books:
.  ..  40723.txt.utf-8

./adequate_books:
.  ..  44578.txt.utf-8  46804-0.txt  more_books

./adequate_books/more_books:
.  ..  1023.txt.utf-8  .secret

./adequate_books/more_books/.secret:
.  ..  deeper_secrets

./adequate_books/more_books/.secret/deeper_secrets:
.  ..  deepest_secrets

./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets:
.  ..  uber-secret.txt

./satisfactory_books:
.  ..  16021.txt.utf-8  23765.txt.utf-8  more_books

./satisfactory_books/more_books:
.  ..  37121.txt.utf-8
georgiana@georgiana:~/Downloads/files$ cd adequate_books/
georgiana@georgiana:~/Downloads/files/adequate_books$ cd more_books/
georgiana@georgiana:~/Downloads/files/adequate_books/more_books$ cd .secret/
georgiana@georgiana:~/Downloads/files/adequate_books/more_books/.secret$ cd deeper_secrets/
georgiana@georgiana:~/Downloads/files/adequate_books/more_books/.secret/deeper_secrets$ cd deepest_secrets/
georgiana@georgiana:~/Downloads/files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets$ ls
uber-secret.txt
georgiana@georgiana:~/Downloads/files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets$ cat uber-secret.txt 
picoCTF{f1nd_15_f457_ab443fd1}

9. Big Zip - picoCTF{gr3p_15_m4g1c_ef8790dc}

georgiana@georgiana:~/Downloads$ egrep -r "pico"
flag:picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}
Binary file strings matches
file:picoCTF{grep_is_good_to_find_things_dba08a45}
runme.py:flag ='picoCTF{run_s4n1ty_run}'
folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
Binary file static matches
Binary file Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet matches
Binary file files.zip matches
files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt:picoCTF{f1nd_15_f457_ab443fd1}
files/14789.txt.utf-8:brassa un picotin d'orge_. Comme depuis une demi-heure environ c'était
Binary file strings(1) matches
Binary file warm matches


10. Based - picoCTF{learning_about_converting_values_00a975ff}
Am avut de facut transformari din binar, octal si hexa si text.

georgiana@georgiana:~$ nc jupiter.challenges.picoctf.org 29221
Let us see how data is stored
lamp
Please give the 01101100 01100001 01101101 01110000 as a word.
...
you have 45 seconds.....

Input:
lamp
Please give me the  155 141 160 as a word.
Input:
map
Please give me the 70656172 as a word.
Input:
pear
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_00a975ff}


11. plumbing - picoCTF{digital_plumb3r_06e9d954}

georgiana@georgiana:~$ nc jupiter.challenges.picoctf.org 7480 | egrep "pico"
picoCTF{digital_plumb3r_06e9d954}


12. mus1c - picoCTF{rrrocknrn0113r}
Mi-a fost dat un fisier text in care pe fiecare linie erau mai multe cuvinte.
Am prelaut intregul text si l-am introdus intr-un interpretor care mi-a generat urmatorul sir:
114
114
114
111
99
107
110
114
110
48
49
49
51
114
Acest sir l-am transformat in text, fiecare numar reprezentand un caracter si am obtinut rrrocknrn0113r, iar raspunsul l-am scris sub forma standard.


13. flag_shop - picoCTF{m0n3y_bag5_9c5fac9b}

georgiana@georgiana:~/Downloads$ nc jupiter.challenges.picoctf.org 4906

14. 1_wanna_b3_a_r0ck5tar - picoCTF{BONJOVI}
Am folosit un interpretor care transforma cuvintele in numere zecimal, care la randul lor vor reprezenta un anumit caracter.

Rocknroll is right              
Silence is wrong                
A guitar is a six-string        
Tommy's been down               
Music is a billboard-burning razzmatazz!
Listen to the music             
If the music is a guitar                  
Say "Keep on rocking!"                
Listen to the rhythm
If the rhythm without Music is nothing
Tommy is rockin guitar
Shout Tommy!                    
Music is amazing sensation 
Jamming is awesome presence
Scream Music!                   
Scream Jamming!                 
Tommy is playing rock           
Scream Tommy!       
They are dazzled audiences                  
Shout it!
Rock is electric heaven                     
Scream it!
Tommy is jukebox god            
Say it!                                     
Break it down
Shout "Bring on the rock!"
Else Whisper "That ain't it, Chief"                 
Break it down 


15. PW Crack 1 - picoCTF{545h_r1ng1ng_56891419}
Parola cautata era scrisa in conditia de verificare in script

georgiana@georgiana:~/Downloads$ python3 level1.py
Please enter correct password for flag: 691d
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419}

16. PW Crack 2 - picoCTF{545h_r1ng1ng_56891419}
