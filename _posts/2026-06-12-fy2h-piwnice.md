---
layout: page
title: Odbiór zdjęć satelitarnych przez radioteleskop RT-4
date: 2026-06-12
author: Paweł Skrzypkowski, SQ2IPS
category: projekty
---

W tym tygodniu ja (Paweł SQ2IPS) miałem przyjemność być obecnym na obozie w Obserwatorium Astronomiczne UMK w Piwnicach organizowanym przez Fundusz Zdolni. W tym miejscu mieści się największy radioteleskop w Środkowej Europie czyli RT4, którego czasza mierzy 32m. Jest on stale wykorzystywany przez UMK do badania m. in. maserów metanolowych czy zjawiska szybkich błysków radiowych (FRB). Poza tym jest częścią Europejskiej sieci interferometrycznej EVN.

Podczas pobytu miałem możliwość skorzystać z okna czasowego radioteleskopu aby podłączyć się do systemu odbiorczego z użyciem SDR'a i przeprowadzić nasłuchy satelitarne.

![SDR](/assets/images/phocagallery/FY-2H/2026-06-10-17-58-35-606.jpg)

![RT4](/assets/images/phocagallery/FY-2H/2026-06-12-13-53-32-690.jpg)

Z możliwych do wykorzystania pasm, które mają przeznaczenie w komunikacji satelitarnej zostało niestety tylko pasmo L co oznaczało, że jedynymi obiektami nieruchomymi (śledzenie obiektów z wysoką prędkością nie jest możliwe), z których można będzie coś zdekodować będą satelity pogodowe. Wybrałem więc FengYun-2H z racji swojej wysokiej rozdzielczości (10000x10000 pikseli). Nadaje on pełnoklatkowe zdjęcia ziemi w 5 zakresach: 1 widzialnym i 4 podczerwonych.

![orbit](/assets/images/phocagallery/FY-2H/orbit.png)

Po ustawieniu anteny oraz pasma pojawił się bardzo silny sygnał co było zdecydowanie oczekiwane przy antenie tej klasy. Do odbioru sygnału i jego zdekodowania użyłem programu [SatDump](https://www.satdump.org/).

![SatDump](/assets/images/phocagallery/FY-2H/Screenshot_20260612_001119.png)

Udało się odebrać takie oto zdjęcia (zdjęcia z kanału widzialnego, pokolorowane):

![fy2](/assets/images/phocagallery/FY-2H/fy2-svissr_False_Color.png)

![fy2-1](/assets/images/phocagallery/FY-2H/fy2-svissr1_False_Color.png)

Tutaj kilka zbliżeń (kompresja jpg):

![fy2-frag1](/assets/images/phocagallery/FY-2H/fy2-svissr_False_Color_frag1.jpg)

![fy2-frag2](/assets/images/phocagallery/FY-2H/fy2-svissr_False_Color_frag2.jpg)

![fy2-frag3](/assets/images/phocagallery/FY-2H/fy2-svissr_False_Color_frag3.jpg)

![fy2-frag4](/assets/images/phocagallery/FY-2H/fy2-svissr_False_Color_frag4.jpg)

![fy2-frag](/assets/images/phocagallery/FY-2H/fy2-svissr1_False_Color_frag.jpg)

A tutaj połączone wszystkie kanały przeniesione w zakres widzialny:

![fy2-ev](/assets/images/phocagallery/FY-2H/fy2-svissr_S-VISSR_EView.jpg)