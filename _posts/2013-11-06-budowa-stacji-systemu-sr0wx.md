---
layout: page
title: Budowa stacji systemu SR0WX
date: 2013-11-06
author: Jędrzej Marsz, SQ2DK
category: projekty
subcategory: sr0wx
---

Obecnie z siedziby klubu pracuje stacja systemu SR0WX.
Stacja ta, podaje tekstem bierzącą oraz prognozowaną pogodę oraz inne wybrane warunki dla naszego regionu na częstotliwości 144.950MHz (FM). Komunikaty podawane są co około 15 minut.
Porgramowo stację przygotował i oprogramował Paweł SQ2IPS. Szczegóły programu oraz kod można uzyskać na stronie [github.com](https://github.com/sq2ips/sr0wx). Kod został mocno zmienony i unowocześniony w stosunku do orginalnego kodu systemu SR0WX. Dodane zostały też nowe moduły pozwalające na rozszerzenie spektrum komunikatów.
Sprzętowo stacja oparta jest o Rapberry Pi 3B pracujące pod kontrolą systemu Linux. Nadajnik stanowi radiotelefon Motorola GM350. Antena Diamond X-300 na szycie około 4m masztu zamontowana jest na budynku Akademika, w którym mieści się siedziba klubu.
 
 
A tak o ówczesnej stacji pisaliśmy przeszło 10 lat temu...
W klubie trwają przygotowania do uruchomienia stacji nadającej fonią komunikaty pogodowe działającą w ramach systemu [SR0WX](https://vhf.com.pl/stacja-pogodowa-sr0wx-py).

Sprzęt w części został już przygotowany i skonfigurowany.

W chwili obecnej sprzęt składa się z:

- Zasilacza: popularnego zasilacza 12V z XBox-a Microsoft DPSN-216BB-1A(pozbawiony plastikowej obudowy)
- Transceivera: Talco ER16 (moc nadajnika około 10W) przestrojone na 144,950MHz
- Komputera: Terminal WYSE V90 z systemem Linux

Wymienione wyżej elementy zostały upakowane w aluminiowej obudowie typu rack. Wyjście karty dźwiękowej terminala połączone jest z wejściem mikrofonowym radiotelefonu, sterowanie nadawaniem realizowane jest zaś przy pomocy zmiany stanu na liniach CTS/RTS portu szeregowego.

Sprzęt został dość ciasno upakowany w środku obudowy, dlatego też konieczne było wymuszenie wentylacji przez zainstalowanie wentylatora na tylnej ściance obudowy. W obudowie zostało przewidziane miejsce na jeszcze jeden mały radiotelefon (z pasma CB).

Wkrótce przewidujemy testowe uruchomienie stacji z siedziby klubu.
 
Zdjęcia terminala oraz radia:
