---
layout: post
title: Kontroler stacji
date: 2023-12-29
author: Jędrzej Marsz, SQ2DK
categories: 
  - Projekty techniczne
---

Zgodnie z założeniami, stacja naziemna SP2ZIE ma posiadać przedwzmacniacz antenowy (LNA) wraz z filtrem pasmowym umieszczone przy samej antenie. Wymusza to przełączanie nadawanie / odbiór, gdyż moc nadajnika może zniszczyć przedwzmacniacz. Zdecydowano się też na zastosowanie oddzielnego toru kablowego (kabli koncentrycznych) nadawczego oraz odbiorczego.

![kontroler top 1](/assets/images/phocagallery/2023_12_PW_sat3/kontroler_top_1.jpg)

Umożliwia to umieszczenie dodatkowego filtra pasmowego oraz dzielnika sygnału odbieranego w pobliżu urządzenia nadawczo-odbiorczego. Zastosowanie dodatkowych elementów jak przekaźniki w.cz., przestrajane elektromechanicznie filtr pasmowy itp. wymaga zastosowanie urządzenia sterującego – kontrolera. Kontroler ten realizuje następujące funkcje:

- sterowanie procesem przełączaniem nadawanie-odbiór – po otrzymaniu od radia żądania nadawania, przełącza odpowiednie przekaźniki koncentryczne oraz oczekuje na sygnały zwrotne, odczekuje odpowiedni czas i zwraca do radia sygnał zezwalający na transmisję.
- sterowanie przestrajaniem wąskopasmowego filtra w.cz.
- sterowanie przekaźnikiem omijającym wąskopasmowy filtr w.cz.
- sterowanie regulowanym tłumikiem w.cz. (w tej chwili nie wykorzystane)
- obsługa przycisków i enkodera oraz wyświetlanie funkcji na panelu lokalnym
- obsługa sterowania przez port szeregowy współpraca z komputerem)

W celu realizacji opisanych funkcji zaprojektowany został układ elektroniczny składający się z zestaw ewaluacyjny z mikrokontrolerem STM32F103C8T6 (Bluepill), drivera silnika krokowego, konwertera DC-DC (step-up) do sterowania przekaźnikiem, oraz układu elektronicznego składający się głównie z tranzystorów mosfet oraz bipolarnych realizujący sterowanie przekaźnikami. Schemat układu można zobaczyć poniżej.


![kontroler schemat](/assets/images/phocagallery/2023_12_PW_sat3/kontroler_schemat.png)

Oprogramowanie mikrokontrolera zostało stworzone w środowisku Arduino. Zarówno kod jak i schemat dostępny jest pod adresem:

[https://github.com/sq2dk/GS-Schooner](https://github.com/sq2dk/GS-Schooner)

Płytka wraz z pozostałymi elementami urządzenia zostały umieszczone w wykonanej obudowie o wielkości 4U, przewidzianej do montażu w szafie rack.

![kontroler tyl 2](/assets/images/phocagallery/2023_12_PW_sat3/kontroler_tyl_2.jpg)

![kontroler pcb 1](/assets/images/phocagallery/2023_12_PW_sat3/kontroler_pcb_1.jpg)

![kontroler panel 1](/assets/images/phocagallery/2023_12_PW_sat3/kontroler_panel_1.jpg)
