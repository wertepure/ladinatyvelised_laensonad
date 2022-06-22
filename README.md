# Eesti omasõnade ja ladinatüveliste laensõnade kasutuse võrdlemine
Siin repositooriumis on digihumanitaaria projekti raames koostatud kood eesti omasõnade ja ladinatüveliste laensõnade kasutuse võrdlemiseks. Uurimise all on sõnad, millel on eesti omasõna ja vastav samatähenduslik ladinatüveline laen. Kood otsib Digari ajakirjandustekstidest tekste, kus otsitavaid sõnu on mainitud, salvestab need failidena ja koostab nende failide tulemusel oma- ja laensõnade kasutussageduse võrdlemiseks graafikud ja tabelid. Lisaks saab leida väljaanded, kus need sõnad kõige rohkem esinesid ja nende sagedustest graafikud teha.<br>

Failis ladina_tyved_kood.ipnyb on kood Jupyter Notebooki kujul, mida saab kasutada Jupyteri keskkonnas.<br>

# Juhised koodi kasutamiseks:
Laadige alla ladina_tyved_kood.ipynb ja avage see Jupyteri keskkonnas.
## Failide tegemise blokis:
Searchterm on see sõna, mida tahad otsida.
<br>
Searchfile all saad panna sellele failile nime, kuhu tulemus salvestatakse
<br>
subset_ek on korpuse kõik eestikeelsed tekstid, kust sõna hakatakse otsima
<br>
Lemmatiseeritud tekstide jaoks on see 'searchtype="lemmas"
<br>
Lisage failinimesse, kas ta on omasõna või võõrsõna, nt absoluutne_voorsona.txt, täielik_omasona.txt
<br>
### NB! Kõigile otsingusõnadele lisada ette ja taha \\\b nagu allpool kujutatud. 
Nii välistatakse nt sellised juhud, et otsides sõna 'kamp' leitakse ka 'kampsun'

## Failide lisamine kaustadesse:
Et see töötaks, on vaja teha kõigepealt üks suur kaust, nt 'ladina_tyved'. Seejärel saab lisada sinna alamkaustu. Ühes alamkaustas on ühe mõiste kohta käivad sõnad, mille failinimes peab avalduma, mis tüüpi sõnaga on tegu (kas eesti omasõna või ladina laen, nt 'absoluutne_voorsona.txt', 'täielik_omasona.txt'). Alamkausta nimi, kus need failid on, võiks kajastada kõiki neid sõnu (nt 'absoluutne_täielik'), sest kausta nimi muudetakse hiljem graafiku pealkirjaks.
<br>
### NB! Mõelge täpselt, kuhu tahate tulemusi salvestada. Minul näeb failipuu välja selline:
-kodu <br>
---- ladina_tyved (siin on kood) <br>
-------- graafikud <br>
-------- tabelid <br>
------------ normitud <br>
------------ tavalised <br>
-------- tekstid <br>
------------ absoluutne_täielik <br>
------------------ absoluutne_voorsona.txt <br>
------------------ täielik_omasona.txt <br>
<br>
Kui teil on samasugune failipuu, siis pole vaja koodis midagi muuta. Kui te aga tahaks midagi teisiti teha, otsi koodist sõna 'path' ja leiate kõik kohad, kus seda muuta saad. See keskkond arvestab koduks selle koha, kus kood on, nii et kui tahta nt, et fail salvestatakse kohta "kodu/ladina_tyved/graafikud", peab kirjutama pathiks ainult "graafikud". 
