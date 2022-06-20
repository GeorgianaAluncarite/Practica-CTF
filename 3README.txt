Ziua 3 - 20.06.2022

1. PW Crack 2 - picoCTF{tr45h_51ng1ng_9701e681}

georgiana@georgiana:~/Downloads$ python3 level2.py
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}


2. PW Crack 3 - picoCTF{m45h_fl1ng1ng_cd6ed2eb}

georgiana@georgiana:~/Downloads$ python3 level3.py
Please enter correct password for flag: dba8
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}

3. PW Crack 4 - picoCTF{fl45h_5pr1ng1ng_d770d48c}
Am avut de completat codul level4.py in care am introdus un loop for care sa parcurga toate posibilele parole din pos_pw_list.
Prin intermedul acestui loop programul isi ia singur si testeaza parolele.

import hashlib

### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level4.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level4.hash.bin', 'rb').read()


def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()


def level_4_pw_check(user_pw):
    #user_pw = input("Please enter correct password for flag: ")
    user_pw_hash = hash_pw(user_pw)
    
    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    #print("That password is incorrect")



# The strings below are 100 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["8c86", "7692", "a519", "3e61", "7dd6", "8919", "aaea", "f34b", "d9a2", "39f7", "626b", "dc78", "2a98", "7a85", "cd15", "80fa", "8571", "2f8a", "2ca6", "7e6b", "9c52", "7423", "a42c", "7da0", "95ab", "7de8", "6537", "ba1e", "4fd4", "20a0", "8a28", "2801", "2c9a", "4eb1", "22a5", "c07b", "1f39", "72bd", "97e9", "affc", "4e41", "d039", "5d30", "d13f", "c264", "c8be", "2221", "37ea", "ca5f", "fa6b", "5ada", "607a", "e469", "5681", "e0a4", "60aa", "d8f8", "8f35", "9474", "be73", "ef80", "ea43", "9f9e", "77d7", "d766", "55a0", "dc2d", "a970", "df5d", "e747", "dc69", "cc89", "e59a", "4f68", "14ff", "7928", "36b9", "eac6", "5c87", "da48", "5c1d", "9f63", "8b30", "5534", "2434", "4a82", "d72c", "9b6b", "73c5", "1bcf", "c739", "6c31", "e138", "9e77", "ace1", "2ede", "32e0", "3694", "fc92", "a7e2"]

for pw in pos_pw_list:
	level_4_pw_check(pw)


georgiana@georgiana:~/Downloads$ python3 level4.py 
Welcome back... your flag, user:
picoCTF{fl45h_5pr1ng1ng_d770d48c}


4. PW Crack 5 - picoCTF{h45h_sl1ng1ng_36e992a6}

import hashlib

### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level5.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level5.hash.bin', 'rb').read()


def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()


def level_5_pw_check(user_pw):
    #user_pw = input("Please enter correct password for flag: ")
    user_pw_hash = hash_pw(user_pw)
    
    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    #print("That password is incorrect")


#modificarile aduse de mine

with open("/home/georgiana/Downloads/dictionary.txt") as dictionary:
	lines = dictionary.readlines()
	for line in lines:
		line = line.strip()
		level_5_pw_check(line)


georgiana@georgiana:~/Downloads$ python3 level5.py 
Welcome back... your flag, user:
picoCTF{h45h_sl1ng1ng_36e992a6}


5. Stonks - picoCTF{I_l05t_4ll_my_m0n3y_bdc425ea}

georgiana@georgiana:~/Downloads$ nc mercury.picoctf.net 53437
Welcome back to the trading app!

What would you like to do?
1) Buy some stonks!
2) View my portfolio
1
Using patented AI algorithms to buy stonks
Stonks chosen
What is your API token?
%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x
Buying stonks with token:
980e3b0804b00080489c3f7f86d80ffffffff1980c160f7f94110f7f86dc70980d180c980e390980e3b06f6369707b465443306c5f49345f74356d5f6c6c306d5f795f79336e3463646261653532ffdc007df7fc1af8f7f9444059ab070010f7e23ce9f7f950c0f7f865c0f7f86000ffdc85e8f7e1468df7f865c08048ecaffdc85f40f7fa8f09
Portfolio as of Sun Jun 19 16:04:45 UTC 2022


12 shares of KTDF
2 shares of Y
1 shares of M
1 shares of E
1335 shares of FY
125 shares of FKU
Goodbye!

#Am preluat sirul de caractere generat si l-am pus intr-un convertor hex to text si printre altele am obtinut un string asemanator cu flag ul cautat:

georgiana@georgiana:~/Downloads$ python3
Python 3.8.10 (default, Mar 15 2022, 12:22:08) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> s = "ocip{FTC0l_I4_t5m_ll0m_y_y3n4cdbae52  }"
>>> for x in range(0, len(s), 4):
...     print(s[x+3]+s[x+2]+s[x+1]+s[x],end="")
... 
Traceback (most recent call last):
  File "<stdin>", line 2, in <module>
IndexError: string index out of range
picoCTF{I_l05t_4ll_my_m0n3y_bdc425ea}


6. New Caesar - picoCTF{et_tu?_a2da1e18af49f649806988786deb2a6c}
Dupa modelul de criptare din new_caesar.py am creat un nou program in care decriptez mesajul: mlnklfnknljflfmhjimkmhjhmljhjomhmmjkjpmmjmjkjpjojgjmjpjojojnjojmmkmlmijimhjmmj

import string
import binascii
enc ="mlnklfnknljflfmhjimkmhjhmljhjomhmmjkjpmmjmjkjpjojgjmjpjojojnjojmmkmlmijimhjmmj"
ALPHABET = string.ascii_lowercase[:16] 

b16 = []

for i in range(len(ALPHABET)):
	b16.append("")

for i in enc:
    for k in range(len(ALPHABET)):
        index = ALPHABET.index(i)
        if(k <= index):
            b16[k]+=chr(index -k+97)
        else:
            b16[k]+=chr(index +16-k+97)

for k in range(len(ALPHABET)):
    flag=""
    b = b16[k]
    for i in range(0, len(b), 2):
        if(b[i+1] in ALPHABET and b[i] in ALPHABET):
            index1 = ALPHABET.index(b[i])
            index2 = ALPHABET.index(b[i+1])
            flag+= chr((index1 <<4) +index2)
    print(flag)

georgiana@georgiana:~/Downloads$ gedit new_caesar_d.py &
georgiana@georgiana:~/Downloads$ python3 new_caesar_d.py 
et_tu?_a2da1e18af49f649806988786deb2a6c

7. EASY1 - picoCTF{CRYPTOISFUN}
Am creat un program care construieiste flag ul cautat.

from string import ascii_uppercase as letters

key = "SOLVECRYPTO"
encryptedFlag = "UFJKXQZQUNB"

alphabet = []
for i in letters:
    alphabet.append(i)

solvedFlag = []

for v, k in zip(encryptedFlag, key):
    sol = alphabet[alphabet.index(v) - alphabet.index(k)]
    solvedFlag.append(sol)

print("picoCTF{" + ''.join(solvedFlag) + "}")


georgiana@georgiana:~/Downloads$ gedit dec.py &
[2] 17554
georgiana@georgiana:~/Downloads$ python3 dec.py 

picoCTF{CRYPTOISFUN}


8. 13 - picoCTF{not_too_bad_of_a_problem}
Am preluat textul dat in enunt cvpbPGS{abg_gbb_onq_bs_n_ceboyrz} si l-am trecut printr-un decoder ROT13,
iar acesta este rezultatul : picoCTF{not_too_bad_of_a_problem}


9. Dachshund Attacks - picoCTF{proving_wiener_2635457}

import owiener

c = 4582595760185334234856402098368046908625834656973584033103490541987974068876293411882597599275159150262596086023335652472407344221286386171708122328132907607553988570841847089983706387690531031847392673162061472674876153818361359458093591355427908607233615401872173240488216334232093110038548462692397511833
e = 5380370395527417191527227126173070215481811002758251380189160079859808141985901971833297436436479278867511926841797357897672992555636754563410399553027670253017958725822899321395256625419109830436233547840578386741559161856338871760160728678924065406988672241210781262465277695895350444289434040624978626461
n = 77986888238362749259002601393853546022122983371411296193397048925751729761948411850331557277085117943896370588215260852556970429126757219527794125875648667761273733887849578930644990015277625406437748772700737352360947561589217406380047597013760170296373905301216611226384612551867789428046919031733809006321

if d is None:
    print("Failed")

else :
    print("Hacked d = {}".format(d))

M = pow(c, d, n)

print("Decrypted message: ", M)

10. Play Nice - 007d0a696aaad7fb5ec21c7698e4f754

georgiana@georgiana:~$ nc mercury.picoctf.net 30568
Here is the alphabet: 0fkdwu6rp8zvsnlj3iytxmeh72ca9bg5o41q
Here is the encrypted message: herfayo7oqxrz7jwxx15ie20p40u1i
What is the plaintext message? emf57mgc51tp693dtt4g3h7f8ouwq3
Congratulations! Here's the flag: 007d0a696aaad7fb5ec21c7698e4f754


11. Vigenere - picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_d85729g7}
Am citit despre vigenère cipher, apoi mesajul dat (rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_f85729e7}) l-am introdus intr-un decoder de tipul vigenère cipher si am obtinut:
picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_d85729g7}


12. Flags - PICOCTF{F1AG5AND5TUFF}
Am avut nevoie de codurile anumitor steaguri pentru a descifra flag ul.

https://en.wikipedia.org/wiki/International_maritime_signal_flags