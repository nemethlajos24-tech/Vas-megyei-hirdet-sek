# Stabil állapot jegyzet

## Dátum

2026. május 5.

## Jelenlegi működő állapot

Az oldal jelenlegi állapotában működik:

- főoldali hirdetéslista
- kereső
- településszűrő
- kategóriaszűrő
- találatszám kijelzés
- szűrők törlése gomb
- kiemelt hirdetések blokk
- Kiemelt jelzés
- Hívás / Email / Adatlap gombok
- vállalkozói adatlapok
- képes hirdetéskártyák
- kép nélküli hirdetéskártya helykitöltő
- vissza az oldal tetejére gomb
- jogi / információs alsó oldalak
- ADATLAP-KESZITES.md folyamatleírás

## Jelenlegi hirdetések

- Kőszegi Mester Kft.
- Savaria Ízek Étterem
- Lili Szépségszalon
- Autoalkatrace Szombathely
- Vasi Autókozmetika
- Őrségi Otthon Szerviz

## Adatlapok működése

Az adatlapok útvonala:

```text
vallalkozasok/vallalkozas-neve.html

Példák:

vallalkozasok/koszegi-mester-kft.html
vallalkozasok/savaria-izek-etterem.html
vallalkozasok/lili-szepsegszalon.html
vallalkozasok/autoalkatrace-szombathely.html
vallalkozasok/vasi-autokozmetika.html
vallalkozasok/orsegi-otthon-szerviz.html
Képek működése

Főoldali hirdetéskártyánál:

<img src="kepek/vallalkozas-neve.jpg" alt="Vállalkozás neve" class="ad-image">

Ha nincs kép:

<div class="ad-image-placeholder">Vasi Hirdető<br>Kép hamarosan</div>

Vállalkozói adatlapon:

<img src="../kepek/vallalkozas-neve.jpg" alt="Vállalkozás neve" class="profile-image">

Ha nincs kép:

<div class="profile-image-placeholder">Vasi Hirdető<br>Kép hamarosan</div>
Fontos javítás

A hirdetéskártya-sablon már nem sima HTML-megjegyzésként van bent, hanem:

<template id="uj-hirdeteskartya-sablon">
  ...
</template>

Ez azért fontos, mert a sima HTML-megjegyzésen belüli újabb megjegyzés hibát okozhatott, és a hirdetések nem töltődtek be.

Hibajel, amire figyelni kell

Ha az oldalon ez marad kint:

Találatok betöltése...

és nem jelennek meg a hirdetések, akkor valószínűleg HTML szerkezeti hiba van, például:

nyitva maradt HTML-megjegyzés
hiányzó </article>
hiányzó </div>
rossz helyre került sablon
a script előtti HTML rész megszakadt
Jelenlegi stabil állapot neve
Képes kártyák + template javítva, oldal működik
Következő fejlesztések csak ezután

---

## Új stabil állapot

## Dátum

2026. május 12.

## Frissített működő állapot

Az oldal jelenlegi állapotában működik:

- saját domain: https://vasihirdetesek.hu
- HTTPS kényszerítése bekapcsolva
- GitHub Pages domainbeállítás rendben
- Rackhost DNS rekordok beállítva
- Google Űrlap link frissítve
- hirdetésfeladó űrlap működik
- beküldés utáni visszaigazoló üzenet működik
- Vasi Hirdető név Vasi Hirdetések névre frissítve
- régi GitHub Pages link cserélve az új domainre
- hirdetésfeladás résznél emailes kérdésdoboz működik
- Email írása gomb működik
- mobilos nézet első körben javítva
- hirdetéslista, kereső és szűrők működnek
- adatlapok működnek

## Jelenlegi fontos linkek

```text
Weboldal:
https://vasihirdetesek.hu

Google Űrlap:
https://forms.gle/6R44Wh8RiqHY5VNy5

Kapcsolati email:
vasmegyeihirdetesek@gmail.com

---

## Stabil állapot - sablonrendszer bevezetve

## Dátum

2026. május 14.

## Frissített működési rendszer

A Vasi Hirdetések oldalon bevezetésre került a szétbontott ügyfélkezelési és sablonrendszer.

## Új mappák

- `sablonok/`
- `ugyfelek/`

## Új sablonfájlok

- `sablonok/kartya-sablon.html`
- `sablonok/adatlap-sablon.html`
- `sablonok/uj-ugyfel-ellenorzolista.md`
- `sablonok/HASZNALATI-SZABALYOK.md`

## Ügyfél-munkalap rendszer

Minden új vállalkozáshoz külön munkalap készül az `ugyfelek/` mappában.

Első rögzített ügyfél-munkalap:

- `ugyfelek/gampel-domonkos.md`

## Működési szabály

Innentől minden új vállalkozás feltöltése egységes folyamat szerint történik:

1. ügyfél munkalap létrehozása
2. kép feltöltése
3. főoldali kártya létrehozása sablonból
4. adatlap létrehozása sablonból
5. linkek és mobilnézet ellenőrzése
6. ügyfélnyilvántartás frissítése
7. ügyfél visszaigazolása

## Fontos döntés

A vállalkozói adatlapoknál a Kőszegi Mester Kft. adatlapja a mérvadó sablon.

Nem készül minden ügyfélhez külön dizájn, csak a sablonban szereplő adatok, szövegek, képek és linkek cserélődnek.

## Stabil állapot neve

```text
Sablonrendszer és ügyfél-munkalap rendszer bevezetve

