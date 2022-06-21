Ziua 4 - 21.06.2022


1. Morse-code - picoCTF{WH47_H47H_90D_W20U9H7}
Mi-a fost dat un fisier audio pe care am cautat sa il introduc intr-un interpretor pentru codul morse in format audio.


2. credstuff - picoCTF{C7r1F_54V35_71M3}

georgiana@georgiana:~$ cd Downloads/
georgiana@georgiana:~/Downloads$ cd leak/
georgiana@georgiana:~/Downloads/leak$ egrep "cult" usernames.txt
cultiris
smallfaculty
georgiana@georgiana:~/Downloads/leak$ egrep -n "cult" usernames.txt
378:cultiris
406:smallfaculty

Parola pentru user ul cultiris se afla la pozitia 378 in passwords.txt
cvpbPGS{P7e1S_54I35_71Z3}

Acest flag il decriptam cu ajutorul decriptorului ROT13.
picoCTF{C7r1F_54V35_71M3}


3. Rail fence - picoCTF{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_83F6D8D7}
Am citit despre codarea/decodarea Rail fence si apoi am aplicat algoritmul pentru sirul dat : Ta _7N6D8Dhlg:W3D_H3C31N__387ef sHR053F38N43DFD i33___N6

The flag is: WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_83F6D8D7

T	a	~	_	7	N	6	D	8	D	
 h   l g   : W   3 D   _ H   3 C   3 1   N _   _ 3   8 7
  e f   ~ s   H R   0 5   3 F   3 8   N 4   3 D   F D   
   ~     i     3     3     _     _     _     N     6

~ - spatiu


4. Substitution0 - PICOCTF{5UB5717U710N_3V0LU710N_03055505}

key: QWITJSYHXCNDFERMUKGOPVALBZ
initial_text: 
Hjkjpmre Djykqet qkrgj, axoh q ykqvj qet goqojdb qxk, qet wkrpyho fj ohj wjjodj
skrf q ydqgg iqgj xe ahxih xo aqg jeidrgjt. Xo aqg q wjqpoxspd giqkqwqjpg, qet, qo
ohqo oxfj, penerae or eqopkqdxgog—rs irpkgj q ykjqo mkxzj xe q gixjeoxsxi mrxeo
rs vxja. Ohjkj ajkj oar krpet wdqin gmrog ejqk rej jlokjfxob rs ohj wqin, qet q
drey rej ejqk ohj rohjk. Ohj giqdjg ajkj jlijjtxeydb hqkt qet ydrggb, axoh qdd ohj
qmmjqkqeij rs wpkexghjt yrdt. Ohj ajxyho rs ohj xegjio aqg vjkb kjfqknqwdj, qet,
oqnxey qdd ohxeyg xeor iregxtjkqoxre, X irpdt hqktdb wdqfj Cpmxojk srk hxg rmxexre
kjgmjioxey xo.

Ohj sdqy xg: mxirIOS{5PW5717P710E_3V0DP710E_03055505}

decrypted_text: 
HEREUPON LEGRAND AROSE, WITH A GRAVE AND STATELY AIR, AND BROUGHT ME THE BEETLE FROM A GLASS CASE IN WHICH IT WAS ENCLOSED. 
IT WAS A BEAUTIFUL SCARABAEUS, AND, AT THAT TIME, UNKNOWN TO NATURALISTS--OF COURSE A GREAT PRIZE IN A SCIENTIFIC POINT OF VIEW. 
THERE WERE TWO ROUND BLACK SPOTS NEAR ONE EXTREMITY OF THE BACK, AND A LONG ONE NEAR THE OTHER. 
THE SCALES WERE EXCEEDINGLY HARD AND GLOSSY, WITH ALL THE APPEARANCE OF BURNISHED GOLD. 
THE WEIGHT OF THE INSECT WAS VERY REMARKABLE, AND, TAKING ALL THINGS INTO CONSIDERATION, I COULD HARDLY BLAME JUPITER FOR HIS OPINION RESPECTING IT.
THE FLAG IS: PICOCTF{5UB5717U710N_3V0LU710N_03055505}


5. Substitution1 - PICOCTF{FR3QU3NCY_4774CK5_4R3_C001_7AA384BC}

key: QWITJSYHXCNDFERMUKGOPVALBZ
initial_text:
WYHg (gzray hra wimybas yzs hvij) ias i yums rh wrombysa gswbakyu wromsykykrl. 
Wrlysgyilyg ias masgslysn dkyz i gsy rh wzivvsljsg dzkwz ysgy yzska wasiykxkyu, yswzlkwiv (iln jrrjvklj) gckvvg, iln marqvso-grvxklj iqkvkyu. 
Wzivvsljsg bgbivvu wrxsa i lboqsa rh wiysjraksg, iln dzsl grvxsn, siwz uksvng i gyaklj (wivvsn i hvij) dzkwz kg gbqokyysn yr il rlvkls gwraklj gsaxkws. 
WYHg ias i jasiy diu yr vsial i dkns iaaiu rh wrombysa gswbakyu gckvvg kl i gihs, vsjiv slxkarlosly, iln ias zrgysn iln mviusn qu oilu gswbakyu jarbmg iarbln yzs dravn hra hbl iln maiwykws. 
Hra yzkg marqvso, yzs hvij kg: mkwrWYH{HA3FB3LWU_4774WC5_4A3_W001_7II384QW}

decrypted_text: 
CTFS (SHORT FOR CAPTURE THE FLAG) ARE A TYPE OF COMPUTER SECURITY COMPETITION. 
CONTESTANTS ARE PRESENTED WITH A SET OF CHALLENGES WHICH TEST THEIR CREATIVITY, TECHNICAL (AND GOOGLING) SKILLS, AND PROBLEM-SOLVING ABILITY. 
CHALLENGES USUALLY COVER A NUMBER OF CATEGORIES, AND WHEN SOLVED, EACH YIELDS A STRING (CALLED A FLAG) WHICH IS SUBMITTED TO AN ONLINE SCORING SERVICE. 
CTFS ARE A GREAT WAY TO LEARN A WIDE ARRAY OF COMPUTER SECURITY SKILLS IN A SAFE, LEGAL ENVIRONMENT, AND ARE HOSTED AND PLAYED BY MANY SECURITY GROUPS AROUND THE WORLD FOR FUN AND PRACTICE. 
FOR THIS PROBLEM, THE FLAG IS: PICOCTF{FR3QU3NCY_4774CK5_4R3_C001_7AA384BC}


6. Substitution2 - PICOCTF{N6R4M_4N41Y515_15_73D10U5_702F03FC}

key: QWITJSYHXCNDFERMUKGOPVALBZ
initial_text:
xidcddhsgxgdqdcjvwxidczdvvdgxjyvsgidrisoigtiwwvtwufbxdcgdtbcsxltwufdxsxswpgsptvbrspotlydcfjxcswxjprbgtlydctijvvdpodxidgdtwufdxsxswpgawtbgfcsujcsvlwpglgxdugjruspsgxcjxswpabprjudpxjvgzistijcdqdclbgdabvjprujcmdxjyvdgmsvvgiwzdqdczdydvsdqdxidfcwfdcfbcfwgdwajisoigtiwwvtwufbxdcgdtbcsxltwufdxsxswpsgpwxwpvlxwxdjtiqjvbjyvdgmsvvgybxjvgwxwodxgxbrdpxgspxdcdgxdrspjprdhtsxdrjywbxtwufbxdcgtsdptdrdadpgsqdtwufdxsxswpgjcdwaxdpvjywcswbgjaajscgjprtwudrwzpxwcbppspotidtmvsgxgjprdhdtbxspotwpasogtcsfxgwaadpgdwpxidwxidcijprsgidjqsvlawtbgdrwpdhfvwcjxswpjprsufcwqsgjxswpjprwaxdpijgdvdudpxgwafvjlzdydvsdqdjtwufdxsxswpxwbtispowpxidwaadpgsqddvdudpxgwatwufbxdcgdtbcsxlsgxidcdawcdjydxxdcqdistvdawcxdtidqjpodvsguxwgxbrdpxgspjudcstjpisoigtiwwvgabcxidczdydvsdqdxijxjpbprdcgxjprspowawaadpgsqdxdtipsnbdgsgdggdpxsjvawcuwbpxspojpdaadtxsqdrdadpgdjprxijxxidxwwvgjprtwpasobcjxswpawtbgdptwbpxdcdrsprdadpgsqdtwufdxsxswpgrwdgpwxvdjrgxbrdpxgxwmpwzxidscdpduljgdaadtxsqdvljgxdjtispoxiduxwjtxsqdvlxispmvsmdjpjxxjtmdcfstwtxasgjpwaadpgsqdvlwcsdpxdrisoigtiwwvtwufbxdcgdtbcsxltwufdxsxswpxijxgddmgxwodpdcjxdspxdcdgxsptwufbxdcgtsdptdjuwpoisoigtiwwvdcgxdjtispoxidudpwboijywbxtwufbxdcgdtbcsxlxwfsnbdxidsctbcswgsxluwxsqjxspoxiduxwdhfvwcdwpxidscwzpjprdpjyvspoxiduxwydxxdcrdadprxidscujtispdgxidavjosgfstwTXA{P6C4U_4P41L515_15_73R10B5_702A03AT}

decrypted_text: 
THEREEXISTSEVERALOTHERWELLESTABLISHEDHIGHSCHOOLCOMPUTERSECURITYCOMPETITIONSINCLUDINGCYBERPATRIOTANDUSCYBERCHALLENGETHESECOMPETITIONSFOCUSPRIMARILYONSYSTEMSADMINISTRATIONFUNDAMENTALSWHICHAREVERYUSEFULANDMARKETABLESKILLSHOWEVERWEBELIEVETHEPROPERPURPOSEOFAHIGHSCHOOLCOMPUTERSECURITYCOMPETITIONISNOTONLYTOTEACHVALUABLESKILLSBUTALSOTOGETSTUDENTSINTERESTEDINANDEXCITEDABOUTCOMPUTERSCIENCEDEFENSIVECOMPETITIONSAREOFTENLABORIOUSAFFAIRSANDCOMEDOWNTORUNNINGCHECKLISTSANDEXECUTINGCONFIGSCRIPTSOFFENSEONTHEOTHERHANDISHEAVILYFOCUSEDONEXPLORATIONANDIMPROVISATIONANDOFTENHASELEMENTSOFPLAYWEBELIEVEACOMPETITIONTOUCHINGONTHEOFFENSIVEELEMENTSOFCOMPUTERSECURITYISTHEREFOREABETTERVEHICLEFORTECHEVANGELISMTOSTUDENTSINAMERICANHIGHSCHOOLSFURTHERWEBELIEVETHATANUNDERSTANDINGOFOFFENSIVETECHNIZUESISESSENTIALFORMOUNTINGANEFFECTIVEDEFENSEANDTHATTHETOOLSANDCONFIGURATIONFOCUSENCOUNTEREDINDEFENSIVECOMPETITIONSDOESNOTLEADSTUDENTSTOKNOWTHEIRENEMYASEFFECTIVELYASTEACHINGTHEMTOACTIVELYTHINKLIKEANATTACKERPICOCTFISANOFFENSIVELYORIENTEDHIGHSCHOOLCOMPUTERSECURITYCOMPETITIONTHATSEEKSTOGENERATEINTERESTINCOMPUTERSCIENCEAMONGHIGHSCHOOLERSTEACHINGTHEMENOUGHABOUTCOMPUTERSECURITYTOPIZUETHEIRCURIOSITYMOTIVATINGTHEMTOEXPLOREONTHEIROWNANDENABLINGTHEMTOBETTERDEFENDTHEIRMACHINES
THE FLAG IS PICOCTF{N6R4M_4N41Y515_15_73D10U5_702F03FC}


7. transposition-trial - picoCTF{7R4N5P051N6_15_3XP3N51V3_109AB02E}
The flag is picoCTF{7R4N5P051N6_15_3XP3N51V3_109AB02E}

heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V091B0AE}2

het -> the
fl  -> _fl
g a -> ag_ 
s i -> is_
icp -> pic
CTo -> oCT
{7F -> F{7
4NR -> R4N
P05 -> 5P0
1N5 -> 51N
_16 -> 6_1
_35 -> 5_3
P3X -> XP3
51N -> N51
3_V -> V3_
091 -> 109
B0A -> AB0
E}2 -> 2E}

8. Insp3ct0r - picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?832b0699}

Cele 3 parti de flag au fost disperasate in parti diferite ale codului:

<!-- Html is neat. Anyways have 1/3 of the flag: picoCTF{tru3_d3 -->
/* You need CSS to make pretty pages. Here's part 2/3 of the flag: t3ct1ve_0r_ju5t */
/* Javascript sure is neat. Anyways part 3/3 of the flag: _lucky?832b0699} */


9. Scavenger Hunt - picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_7a46d25d}

Cele 3 parti de flag au fost disperasate in parti diferite ale codului:

Here's the first part of the flag: picoCTF{t
/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */
Pentru a afla cea de-a treia parte am accesat aceasta adresa http://mercury.picoctf.net:44070/robots.txt
User-agent: *
Disallow: /index.html
# Part 3: t_0f_pl4c
# I think this is an apache server... can you Access the next flag?
Pentru a afla cea de-a patra parte am accesat aceasta adresa http://mercury.picoctf.net:44070/.htaccess
# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.
Pentru a afla cea de-a patra parte am accesat aceasta adresa http://mercury.picoctf.net:44070/.DS_Store
Congrats! You completed the scavenger hunt. Part 5: _7a46d25d}

10. Wireshark doo dooo do doo... - picoCTF{p33kab00_1_s33_u_deadbeef}
Am deschis wireshark si am urmarit fluxul si am observat ca a fost transmis acest mesaj: Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs},
mesaj pe care l-am decodificat cu ROT13