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

