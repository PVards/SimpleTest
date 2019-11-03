# Paskaita 1
# Paskaita 2
# Paskaita 3
## Vi redaktorius ir naudojimasis juo
vi - tai texto redaktorius komandinėje eilutėje. Kadangi šis redaktorius yra pritaikytas veikti komandinėje eilutėje, su juo dirbant *nėra naudojama kompiuterinė pelė*. Pradėjus dirbti, su vi redaktoriumi, sesija prasideda *redagavimo režime*. Veikimo režimai yra du: **įvedimo**, bei **redagavimo**.
Įvedimo režimas skirtas įvesti duomenis į failą, kol redagavimo režimas skirtas judėti faile, bei atlikti veiksmus, kaip trynimas, kopijavimas, paieška.  
Norėdami pradėti darbą, įvedame `vi <failas>`, tai atidaro failą, nurodytu <failas\> vardu. Jį atidarius, galima nuspausti klavišą i kad pereiti į įvedimo režimą. baigus teksto įvedimą, iš įvedimo režimo išeinama klavišu Esc.  
Esant redagavimo režime galima vesti komandas. Vartojamos komandos, šiame redaktoriuje, išvardytos sekančiose pastraipose.  
Arba failo išsaugojimui, redaktoriaus išjungimui, arba abiem kartu:  
ZZ - išsaugo failą ir išjungia redaktorių  
:q! - išjungia atšaukiant visus pakeitimus, nuo paskutinio išsaugojimo  
:w - išsaugo failą, neišjungiant redaktoriaus  
:wq - išsaugo failą ir išjungia redaktorių  
Norint perkelti žymeklį:  
:set nu - įjungia eilučių numerių vaizdavimą  
rodykliniai klavišai - judina žymeklį  
j k h l - judina žymeklį žemyn, aukštyn, kairėn, dešinėn  
^ - perkelia žymeklį į eilutės pradžią  
$ - perkelia žymeklį į eilutės pabaigą  
nG - perkelia žymeklį į n eilutę. Nenurodžius numerio, perkelia į paskiausią eilutę  
w - perkelia žymeklį į sekančio žodžio pradžią  
nw - perkelia žymeklį n žodžių pirmyn  
b - perkelia žymeklį į pastarojo žodžio pradžią  
nb - perkelia žymeklį n žodžių atgal  
{ - perkelia žymeklį vienu pastraipa atgal  
} - perkelia žymeklį viena pastraipa pirmyn  
Norint ištrinti simbolius arba simbolių eilutes:  
x - ištrina vieną simbolį  
nx - ištrina n simbolių  
dd - ištrina eilutę  
dn - ištrinti iki pozicijos, nurodytos n žymeklio perkėlimo nurodymu  
Norint atšaukti paskutinius pakeitimus:  
u - atšaukti paskutinį veiksmą  
U - atšaukti visus pakeitimus eilutėje  
Šaltiniai:  
https://ryanstutorials.net/linuxtutorial/vi.php
# Paskaita 4
# Paskaita 5
## Procesai
**Procesas**, tai Linux operacinės sistemos abstrakcija, nusakanti vykdomą kompiuterinę programą. Dabartiniuose kompiuteriuose patikrinus aktyvius procesus, galima rasti, kad jų yra įspūdingai daug, kadangi kompiuteris turi atlikti daug užduočių. Branduolio požiūriu procesą sudaro *atminties vieta* ir *duomenų struktūrų rinkinys*. Pats procesas yra **objektas**, per kurį galima valdyti programos naudojamus išteklius, kaip  
 - Atmintį  
 - Procesoriaus laiką  
 - Ivesties bei išvesties išteklius  
Proceso atmintyje yra saugoma įvairūs duomenys, kaip proceso instrukcijų aprašas, naudojamos bibliotekos, to proceso kintamieji, proceso dėklai, bei papildoma branduoliui reikalinga informacija.  
Paprasčiausias procesas turi tik vieną instrukcijų seką, kuri daugumoje atvejų būna operacinės sistemos dalis, tačiau sudėtingesni gali turėti keletą *gijų*, kad nereiktų, tai pačiai užduočiai atlikti, kelių, tarpusavyje sąveikaujančių, procesų. Kadangi šiuolaikinio vartotojo lūkesčių neįmanoma patenkinti tik vienu procesu, dabartinės operacinės sistemos, kaip LinuxOS, sugeba *daugiaprograminį apdorojimą*. **Daugiaprograminis apdorojimas**, tai yra metodas kuris leidžia kelis procesus pasidalinti tuo pačiu procesoriumi, bei kitais sistemos ištekliais. Kadangi kiekvienas procesorius, daugiabranduolinio procesoriaus atveju kiekvienas branduolys, sugeba atlikti tik vieną procesą tuo pat metu, daugiaprograminis apdorojimas leidžia turėti daugiau aktyvių procesų, nei kompiuteris turi procesorių.  
Kad procesai galėtų bendrauti tarpusavyje, egzistuoja įvairūs *signalai*, kadangi tiesioginis procesų bendravimas gali sukelti saugumo, bei patikimumo spragų.  
Patys procesai pradedami kaip **fork()** išdava. To pavyzdys būtų terminale įvykdyta komanda. Kai terminale nurodoma vykdyti komandą, būna sukuriama apvalkalo kopija, kuri prašo įvykdyti tą pateiktą komandą, kurios išvesties srautą galima matyti tame pačiame terminale. Tai labai svarbu žinoti, kadangi apvalkalo kopijos įgyti kintamieji, *gali būti neprieinami apvalkalui, kuriame tuo metu dirbama*.  
Šaltiniai:  
https://en.wikipedia.org/wiki/Process_(computing)  
https://en.wikipedia.org/wiki/Thread_(computing)
# Paskaita 6