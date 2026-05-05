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
