---
layout: page
title: Radioamatorstwo a misje stratosferyczne
date: 2026-04-19
author: Paweł Skrzypkowski, SQ2IPS
category: projekty
subcategory: balony
---


W radioamatorstwie jedną z rzeczy jaką można się zajmować są szeroko pojęte misje balonowe. Składa się na nie wiele działań, od odbioru radiosond IMGW, kończąc na startach własnych misji.


## Sondaże aerologiczne IMGW
[Instytut Meteorologii i Gospodarki Wodnej (IMGW)](https://imgw.pl/) Prowadzi wiele działań służących modelowaniu meteorologicznemu. Jednym z takich działań są [Sondaże aerologiczne](https://cmm.imgw.pl/?page_id=38637), zwane również radiosondażem. Jego celem jest pomiar temperatury, wilgotności oraz ciśnienia na różnych wysokościach w atmosferze. Z tych danych można następnie stworzyć agramy termodynamiczne (tzw. Skew-T). Na ich podstawie można już prowadzić analizę panujących warunków atmosferycznych, prądów powietrznych i przygotowywać m.in. prognozy pogody.


## Czym są radiosondy?
Do takiego sondowania wykorzystuje się tzw. radiosondy, czyli urządzenia, które posiadają czujniki zdolne odczytywać potrzebne parametry, są zasilane bateryjne a zebrane dane wysyłają drogą radiową. Takie sondy umieszcza się pod balonami stratosferycznymi, zrobionymi z latexu i gumy. Takie balony wypełnia się zazwyczaj wodorem i podczepia do nich radiosonde. Całość wznosi się aż do stratosfery na około 30-40km. Tam przez różnice ciśnień balon pęka, a radiosonda spada powtórnie na ziemię. Przez wiatry ląduje jednak daleko od miejsca startu, często nawet setki kilometrów.


## Poszukiwanie radiosond
Taka sonda po pęknięciu balonu nie jest już obiektem zainteresowania IMGW, jej misja jest już zakończona a samo użądzenie uznane za elektrośmieć. W tym momencie wkraczają jednak radioamatorzy. Protokół radiosondy nie jest w żaden sposób szyfrowany i został rozpracowany, powstało wiele programów zdolnych odkodowywać dane przesyłane przez taką sondę. Jednym z najbardziej rozwiniętych z nich jest [radiosonde_auto_rx](https://github.com/projecthorus/radiosonde_auto_rx) potrafi dekodować większość typowych radiosond używanych na świecie. Do jego uruchomienia potrzebny jest tylko komputer, antena oraz [SDR](https://pl.wikipedia.org/wiki/Radio_programowalne). Dane odczytywane przez ten program trafiają domyślnie do centralnej bazy radiosond czyli [SondeHub](https://sondehub.org/). Tam można śledzić na żywo większość radiosond z całego świata, analizować pozyskane z nich dane czy obserwować planowane miejsce updaku. Każdy może więc wybrać się po taką sondę gdy spadła i ją podjąć.


## Co można zrobić z radiosondą?
Gdy udało się już taką radiosonde znaleźć jest kilka opcji. Samo urządzenie to kombinacja mikrokontrolera z czujnikami, modułem GPS, radiowym i innymi. Elementy te można wylutować i zastosować w innych projektach. Ciekawszym rozwiązaniem jest jednak ponowne wykorzystanie całej takiej radiosondy. Do różnych modeli istnieją gotowe zamienniki firmware przeobrażające takie sondy z urządzeń typowo profesjonalnych do trackerów amatorskich mogących spełniać różne funkcje. Do najpopularniejszych należą:
- [RS41ng](https://github.com/mikaelnousiainen/RS41ng) - firmware do radiosond Valsala RS41 będących standardem w większości świata
- [m20-custom-firmware](https://github.com/sq2ips/m20-custom-firmware) - oprogramowanie do sond Meteomodem M20, używanych głównie we Francji oraz Polsce, rozwijany w naszym klubie


## Amatorskie misje balonowe
Takie radiosondy z użyciem odpowiedniego oprogramowania można przeznaczyć do pierwotnego ich celu, czyli lotów stratosferycznych. Tym razem jednak nie profesjonalnych, lecz amatorskich. Taka sonda może nadawać swoje parametry w paśmie amatorskim. Zazwyczaj używa się do tego protokołu [Horus Binary](https://github.com/projecthorus/horusdemodlib), dedykowanego właśnie takim zastosowaniom. Często towarzyszy mu też APRS oraz LoRa. Większość z nich można obserwować w centralnej bazie [Amateru Sondehub](https://amateur.sondehub.org/). Balon podczepia się ponownie pod balon wypełniony wodorem lub helem. Główne typy balonów są dwa. Pierwszy to standardowe Lateksowe, które wznoszą się do stratosfery, potem pękają i spadają. Drugi natomiast stanową balony typu floater. Powłoki takie są wykonane z gumy, której parametry dobrane są tak, że balon wzniesie się na wysokość unoszenia, zazwyczaj około 8km, gdzie będzie się utrzymywać przemieszczany wiatrem.


## Co jest przedmiotem misji amatorskich?
Misje amatorskie mogą mieć wiele celów, najprostszym z nich jest samo śledzenie nadajnika, sprawdzenie jak daleko jest w stanie dolecieć, jednocześnie odczytując parametry z czujników. Do takiego ładunku wystarczy tylko podjęta radiosonda skonfigurowana w odpowiedni sposób oraz źródło zasilania. Można go jednak rozbudować o różne czujniki, chociażby licznik geigera. Inną opcją jest też dodanie nadajnika emitującego obrazki np. w standardzie SSTV, czy nawet kamery przekazującej zdjęcia na żywo.
