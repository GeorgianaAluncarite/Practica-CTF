ZIUA 1 - 16.06.2022

Toate comenzile sunt date dupa ce m-am mutat in directorul Downloads
georgiana@georgiana:~$ cd Downloads


1. Obedient Cat - picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}
Am descarcat fisierul care continea flag ul pe masina virtuala, apoi l-am deschis din terminal cu comanda cat flag.

georgiana@georgiana:~/Downloads$ cat flag


2. Mod 26 - picoCTF{next_time_I'll_try_2_rounds_of_rot13_ZNMldSDw}
Am cautat ce inseamna ROT13. Am citit despre principiul de codare/decodare, apoi am aplicat algoritmul pe sirul de caractere dat (cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_MAZyqFQj})


3. Python Wrangling - picoCTF{4p0110_1n_7h3_h0us3_aa821c16}
Am descarcat cele 3 documente disponibile : script ul in python, flag ul si parola pentru decodarea flag ului.
Am rulat script ul : python3 ende.py -> am avut nevoie de un anumit format pentru decriptarea fisierului in care se afla flag ul : 
python3 ende.py -d flag.txt.en (-d decriptare, pentru ca mesajul era criptat)
Pentru a putea deschide fisierul mi-a fost necesara parola furnizata : aa821c16aa821c16aa821c16aa821c16

georgiana@georgiana:~/Downloads$ python3 ende.py
georgiana@georgiana:~/Downloads$ python3 ende.py -d flag.txt.en
Please enter the password:aa821c16aa821c16aa821c16aa821c16
picoCTF{4p0110_1n_7h3_h0us3_aa821c16}


4. Wave a flag : picoCTF{b1scu1ts_4nd_gr4vy_755f3544}
Am descarcat fisierul pus la dispozitie pentru care a trebuit sa modific permisiunile ca sa pot rula script ul.

georgiana@georgiana:~/Downloads$ ./warm
bash: ./warm: Permission denied				-- in acest punct a trebuit sa adaug permisiuni de execute
georgiana@georgiana:~/Downloads$ chmod u+x warm
georgiana@georgiana:~/Downloads$ ./warm
Hello user! Pass me a -h to learn what I can do!
georgiana@georgiana:~/Downloads$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_755f3544}


5. Information : picoCTF{the_m3tadata_1s_modified}
Am descarcat imaginea cat.jpg. Initial a deschis-o normal, apoi am cautat detalii despre aceasta. Am preluat string ul aferent License care era cel mai apropiat de un flag.
Am transformat string ul gasit (cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9) cu ajutorul functiei base 64.

georgiana@georgiana:~/Downloads$ echo cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 | base64 -d
picoCTF{the_m3tadata_1s_modified}


6. Lets Warm Up : picoCTF{p}
Mi s-a dat o valoare in hexa (0x70) pe care a trebuit sa o transform in ASCII.
Valoarea corespunzatoare lui 0x70 este p. 


7. Warmed Up : picoCTF{61}
A trebuit sa transform 0x3D in baza 10.
Valoarea corespunzatoare lui 0x3D in zecimal este 61. 


8. 2Warm : picoCTF{101010}
A trebuit sa transform 42 in baza 2.
Valoarea corespunzatoare lui 42 in binar este 101010. 


9. The Numbers - PICOCTF{THENUMBERSMASON}
A trebuit sa decodific un mesaj format din numere care reprezentau pozitiile literelor in alfabetul englez.


10. strings it - picoCTF{5tRIng5_1T_827aee91}
Mi-a fost dat un fisier din care a trebuit sa extrag flag ul fara a deschide fisierul.

georgiana@georgiana:~/Downloads$ strings strings | egrep "pico"
picoCTF{5tRIng5_1T_827aee91}


11. Static ain't always noise - picoCTF{d15a5m_t34s3r_1e6a7731}
Mi-a fost dat un fisier binar in care a trebuit sa caut flag ul

georgiana@georgiana:~/Downloads$ strings static | egrep "pico"


12. Tab, Tab, Attack - picoCTF{l3v3l_up!_t4k3_4_r35t!_524e3dc4}
Mi-a fost data o arhiza din care am extras director care continea alte directoare si in final un fisier binar.
M-am mutat in ultimul director (folosind tab) care continea fisierul binar dorit si apoi am cautat flag ul.

georgiana@georgiana:~/Downloads$ cd Addadshashanammu
georgiana@georgiana:~/Downloads/Addadshashanammu$ cd Almurbalarammi/
georgiana@georgiana:~/Downloads/Addadshashanammu/Almurbalarammi$ cd Ashalmimilkala/
georgiana@georgiana:~/Downloads/Addadshashanammu/Almurbalarammi/Ashalmimilkala$ cd Assurnabitashpi/
georgiana@georgiana:~/Downloads/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi$ cd Maelkashishi/
georgiana@georgiana:~/Downloads/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi$ cd Onnissiralis/
georgiana@georgiana:~/Downloads/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis$ cd Ularradallaku/
georgiana@georgiana:~/Downloads/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet
georgiana@georgiana:~/Downloads/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ strings fang-of-haynekhtnamet | egrep "pico"
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_524e3dc4}


13. Bases - picoCTF{l3arn_th3_r0p35}
Mi-a fost dat sirul bDNhcm5fdGgzX3IwcDM1 pe care a trebuit sa il decodific in asa fel incat sa obtin flag ul.


14. First Grep - picoCTF{grep_is_good_to_find_things_dba08a45}
Am descarcat fisierul in care era flag ul, apoi am folosit comanda grep pentru o cautare mai usoara in fisier

georgiana@georgiana:~/Downloads$ egrep "pico" file
picoCTF{grep_is_good_to_find_things_dba08a45}


15. Codebook - picoCTF{c0d3b00k_455157_7d102d7a}

georgiana@georgiana:~/Downloads$ python3 code.py
picoCTF{c0d3b00k_455157_7d102d7a}


16. convertme.py - picoCTF{4ll_y0ur_b4535_762f748e}
Am avut de rulat un script in python pentru care a trebuit sa fac o transformare din zecimal in binar penrtu a obtine flag ul.

georgiana@georgiana:~/Downloads$ python3 convertme.py
If 20 is in decimal base, what is it in binary base?
Answer: 10100
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_762f748e}


17. fixme1.py - picoCTF{1nd3nt1ty_cr1515_09ee727a}

georgiana@georgiana:~/Downloads$ python3 fixme1.py
  File "fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
    ^
IndentationError: unexpected indent

In script am modificat print ul, apoi am mai rulat o data.

georgiana@georgiana:~/Downloads$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}


18. fixme1.py - picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}

georgiana@georgiana:~/Downloads$ python3 fixme2.py
  File "fixme2.py", line 22
    if flag = "":
            ^
SyntaxError: invalid syntax
georgiana@georgiana:~/Downloads$ gedit fixme2.py &		--am modificat semnul pentru conditia de egalitate (din = in ==)
[2] 4681
georgiana@georgiana:~/Downloads$ python3 fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
