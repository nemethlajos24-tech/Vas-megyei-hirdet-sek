# Vállalkozói adatlap készítési folyamat

Ezt a folyamatot kell követni, ha új vállalkozásnak szeretnénk külön adatlapot készíteni a Vasi Hirdető oldalon.

## 1. Új adatlap fájl létrehozása

GitHubon:

Kód → Fájl hozzáadása → Új fájl létrehozása

A fájl neve mindig így nézzen ki:

vallalkozasok/vallalkozas-neve.html

Példák:

vallalkozasok/lili-szepsegszalon.html  
vallalkozasok/savaria-izek-etterem.html  
vallalkozasok/koszegi-mester-kft.html  

Fontos szabályok:

- csak egyszer szerepeljen a `vallalkozasok`
- kisbetű legyen
- ékezet ne legyen
- szóköz helyett kötőjel legyen
- a végén `.html` legyen

Jó példa:

vallalkozasok/savaria-izek-etterem.html

Rossz példa:

vallalkozasok/vallalkozasok/savaria-izek-etterem.html

---

## 2. Sablon használata

Nyisd meg ezt a fájlt:

vallalkozasok/sablon.html

Másold ki a teljes kódját.

Az újonnan létrehozott adatlap fájlba illeszd be.

Ezután cseréld ki az `IDE_...` részeket a vállalkozás adataira.

---

## 3. Kitöltendő adatok

Az adatlapban ezeket kell átírni:

- vállalkozás neve
- település
- kategória
- csomag típusa
- rövid bemutatkozás
- hosszabb bemutatkozás
- főbb szolgáltatások
- ajánlat vagy megjegyzés
- előnyök
- telefonszám
- email cím
- weboldal vagy Facebook link
- nyitvatartás
- szolgáltatási terület

---

## 4. Főoldali hirdetéskártya összekötése az adatlappal

Nyisd meg:

index.html

Keresd meg az adott vállalkozás nevét.

Példa:

Savaria Ízek Étterem

A hirdetéskártyán belül keresd ezt:

<div class="contact-actions">

Az Adatlap sort az Email sor alá, de a lezáró `</div>` elé kell beszúrni.

Példa:

<div class="contact-actions">
  <a class="contact-button" href="tel:+3694555010">Hívás</a>
  <a class="contact-button secondary" href="mailto:rendeles@savariaizek.hu">Email</a>
  <a class="contact-button secondary" href="vallalkozasok/savaria-izek-etterem.html">Adatlap</a>
</div>

---

## 5. Ha még nincs contact-actions rész

Ha a hirdetésnél csak ez van:

<div class="contact">
  <p>☎ +36 94 555 010</p>
  <p>✉ rendeles@savariaizek.hu</p>
</div>

Akkor ezt át kell alakítani ilyenre:

<div class="contact">
  <p>☎ +36 94 555 010</p>
  <p>✉ rendeles@savariaizek.hu</p>
  <p>🌐 https://pelda.hu</p>

  <div class="contact-actions">
    <a class="contact-button" href="tel:+3694555010">Hívás</a>
    <a class="contact-button secondary" href="mailto:rendeles@savariaizek.hu">Email</a>
    <a class="contact-button secondary" href="vallalkozasok/savaria-izek-etterem.html">Adatlap</a>
  </div>
</div>

---

## 6. Mentés

Minden módosítás után:

Változtatások véglegesítése

Ezután meg kell várni, amíg a GitHub Pages frissül.

A frissítést a Műveletek résznél lehet ellenőrizni.

---

## 7. Tesztelés

A főoldalon meg kell nyitni az adott hirdetést, majd rákattintani:

Adatlap

Ha az oldal megnyílik, akkor kész.

Az adatlap közvetlen címe így néz ki:

https://nemethlajos24-tech.github.io/Vas-megyei-hirdet-sek/vallalkozasok/vallalkozas-neve.html

---

## 8. Rövid emlékeztető

Új adatlap készítésénél mindig ezt kell követni:

1. Új fájl: vallalkozasok/valami.html
2. Sablon kód bemásolása
3. IDE_ részek kitöltése
4. index.html-ben vállalkozás megkeresése
5. contact-actions részben Adatlap gomb beszúrása
6. Változtatások véglegesítése
7. Tesztelés az élő oldalon


---

# Új ügyfél felvitele utáni ellenőrzőlista

Ezt minden új vállalkozás felvitele után végig kell ellenőrizni.

## 1. Adatlap ellenőrzése

- [ ] Létrejött az adatlap fájl a `vallalkozasok` mappában
- [ ] A fájlnév kisbetűs
- [ ] A fájlnév ékezet nélküli
- [ ] A fájlnév szóköz helyett kötőjeles
- [ ] A fájl vége `.html`
- [ ] Csak egyszer szerepel az útvonalban a `vallalkozasok`

Jó példa:

```text
vallalkozasok/vasi-autokozmetika.html

2. Adatlap tartalmi ellenőrzése
 A vállalkozás neve jó
 A település jó
 A kategória jó
 A telefonszám jó
 Az email cím jó
 A weboldal / Facebook link jó
 A bemutatkozó szöveg ki van töltve
 A főbb szolgáltatások ki vannak töltve
 A nyitvatartás ki van töltve
 A szolgáltatási terület ki van töltve
 Nem maradt benne IDE_ kezdetű sablonszöveg

Keresés ellenőrzéshez az adatlapban:

IDE_

Ha talál ilyet, akkor még maradt benne sablonos rész.

3. Főoldali hirdetéskártya ellenőrzése

Az index.html fájlban az adott vállalkozás kártyájánál ellenőrizni kell:

 Jó a data-category
 Jó a data-search
 Jó a település
 Jó a vállalkozás neve
 Jó a rövid szolgáltatáscím
 Jó a rövid bemutatkozás
 Jó a látható telefonszám
 Jó a látható email cím
 Jó a weboldal / Facebook sor
4. Gombok ellenőrzése

A hirdetéskártyán belül a contact-actions részben legyen:

<div class="contact-actions">
  <a class="contact-button" href="tel:+36...">Hívás</a>
  <a class="contact-button secondary" href="mailto:...">Email</a>
  <a class="contact-button secondary" href="vallalkozasok/valami.html">Adatlap</a>
</div>

Ellenőrzőlista:

 A Hívás gomb tel: linkje jó
 A telefonszámban a tel: résznél nincs szóköz
 Az Email gomb mailto: linkje jó
 Az Adatlap gomb a jó fájlra mutat
 Az Adatlap linkben szerepel a vallalkozasok/ mappa

Jó példa:

<a class="contact-button secondary" href="vallalkozasok/vasi-autokozmetika.html">Adatlap</a>

Rossz példa:

<a class="contact-button secondary" href="vasi-autokozmetika.html">Adatlap</a>
5. Kategória ellenőrzése

A data-category értéke mindig ezek közül legyen:

epitoipar
vendeglatas
szepseg
auto
otthon
egeszseg
oktatas
bolt
ingatlan
rendezveny
szallas
allatok
penzugy
egyeb

Példák:

data-category="auto"
data-category="szepseg"
data-category="vendeglatas"
6. Élő oldalon tesztelés

Mentés és közzététel után az élő oldalon ellenőrizni kell:

 Megjelent az új hirdetés
 A Hívás gomb működik
 Az Email gomb működik
 Az Adatlap gomb megnyitja az adatlapot
 A kereső megtalálja a vállalkozást név alapján
 A kereső megtalálja szolgáltatás alapján
 A településszűrő megtalálja
 A kategóriaszűrő alatt jó helyen jelenik meg
 Telefonon is jól néz ki
 Számítógépen is jól néz ki
7. Gyors hibakeresés 404 esetén

Ha az Adatlap gombra kattintva 404 hiba jön:

Ellenőrizd az index.html fájlban az Adatlap linket.
Ellenőrizd, hogy a fájl tényleg létezik-e a vallalkozasok mappában.
Ellenőrizd, hogy a fájlnév pontosan ugyanaz-e.
Ellenőrizd az ékezeteket és kötőjeleket.
Ellenőrizd, hogy nincs-e dupla vallalkozasok/vallalkozasok.

Jó útvonal:

vallalkozasok/vallalkozas-neve.html

Hibás útvonal:

vallalkozasok/vallalkozasok/vallalkozas-neve.html
8. Utolsó ellenőrzés mentés előtt

Az index.html fájlban az új kártyánál mindig ellenőrizd:

 <article ...> megvan
 </article> megvan
 <div class="contact"> megvan
 </div> lezárások rendben vannak
 contact-actions rész megvan
 Nem maradt benne régi teszt telefonszám
 Nem maradt benne régi teszt email
 Nem maradt benne IDE_ sablonszöveg

## 3. Mentés

Alul kattints:

**Változtatások véglegesítése**

Ezzel lesz egy külön ellenőrzőlistád minden új ügyfél felviteléhez. Később, ha azt írod, hogy **„új ügyfelet szeretnék f
