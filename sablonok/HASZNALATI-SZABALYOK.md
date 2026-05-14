# Vasi Hirdetések sablonrendszer használati szabályok

## Alapelv

Minden új vállalkozás feltöltése ugyanazon a sémán történik.

Nem írunk minden ügyfélhez új dizájnt.  
A főoldali hirdetéskártyához és az adatlaphoz mindig a meglévő sablonokat használjuk.

## Kötelező sablonok

### Főoldali hirdetéskártya

Sablon:

`sablonok/kartya-sablon.html`

Ezt kell használni minden új főoldali hirdetéshez.

Fontos:
- a `listing-card` class nem módosítható
- a `listing-image` class nem módosítható
- a `listing-title` class nem módosítható
- a `listing-description` class nem módosítható
- a `contact-button` class nem módosítható

### Vállalkozói adatlap

Sablon:

`sablonok/adatlap-sablon.html`

Ez a Kőszegi Mester Kft. adatlapja alapján készült, ez a mérvadó.

Fontos:
- az adatlap szerkezetét nem módosítjuk
- csak az ügyfél adatait, szövegeit, linkjeit és képeit cseréljük
- az Elérhetőségek blokk jobb oldalon marad
- a Bemutatkozás, Főbb szolgáltatások, Miért érdemes őt választani és Szolgáltatási terület blokkok bal oldalon maradnak

## Mappa- és fájlnév szabályok

### Adatlap fájl

Minden adatlap ide kerül:

`vallalkozasok/`

Példa:

`vallalkozasok/gampel-domonkos.html`

Fájlnév szabály:
- kisbetű
- ékezet nélkül
- szóköz helyett kötőjel
- `.html` végződés

### Képek

Minden kép ide kerül:

`kepek/`

Példa:

`kepek/gampel-domonkos-uj.jpeg`

Fájlnév szabály:
- kisbetű
- ékezet nélkül
- szóköz helyett kötőjel
- a kódban pontosan ugyanaz a kiterjesztés legyen, mint a fájlnévben
- `.jpg`, `.jpeg` és `.png` nem ugyanaz

### Ügyfél munkalap

Minden ügyfélhez külön munkalap készül:

`ugyfelek/`

Példa:

`ugyfelek/gampel-domonkos.md`

Ebben szerepel:
- ügyfél alapadatai
- elérhetőségek
- kártya adatai
- adatlap adatai
- képfájl neve
- aktuális állapot
- teendők

## Új ügyfél feltöltési sorrend

1. Űrlapválasz átnézése
2. Ügyfél munkalap létrehozása az `ugyfelek/` mappában
3. Kép feltöltése a `kepek/` mappába
4. Főoldali kártya elkészítése a `sablonok/kartya-sablon.html` alapján
5. Adatlap elkészítése a `sablonok/adatlap-sablon.html` alapján
6. Telefon, email, weboldal / Facebook linkek tesztelése
7. Mobilnézet ellenőrzése
8. Ügyfélnyilvántartás frissítése
9. Visszaigazoló email küldése az ügyfélnek

## Gyakori hibák, amiket kerülni kell

- `ad-card` használata `listing-card` helyett
- `.jpg` írása, miközben a fájl `.jpeg`
- nagybetűs fájlnév használata
- kép feltöltése rossz mappába
- elérhetőségi `href` szövegként való kiírása link helyett
- rossz helyre tett `</div>` vagy `<aside>`
- új adatlap dizájn készítése sablon használata helyett
- hiányzó ügyfél-munkalap

## Alap ellenőrzés publikálás előtt

- [ ] főoldali kártya látszik
- [ ] adatlap megnyílik
- [ ] kép betölt
- [ ] telefon gomb működik
- [ ] email gomb működik
- [ ] Facebook / weboldal gomb működik
- [ ] mobilnézet rendben
- [ ] ügyfélnyilvántartás frissítve
- [ ] ügyfél-munkalap frissítve
