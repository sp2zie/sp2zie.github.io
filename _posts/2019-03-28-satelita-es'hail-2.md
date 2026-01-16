---
layout: post
title: Satelita Es'hail 2
date: 2019-03-28
author: Jędrzej Marsz, SQ2DK
categories: projekty
---

W listopadzie 2018 roku na orbitę wystrzelony został geostacjonarny satelita Es’hail 2. Satelita został skonstruowany przez firmę Mitsubishi Electric na zlecenie rządu Kataru przy udziale Niemieckiego oddziału AMSAT. Poza dostarczaniem sygnału telewizji cyfrowej na sputniku znajduje się również liniowy przekaźnik amatorski. Umożliwia on nawiązywanie dwukierunkowej łączności przez radioamatorów z blisko połowy globu i w nomenklaturze amatorskiej otrzymał nazwę Qatar-OSCAR-100. Przekaźnik przeznaczony jest dla transmisji wąskopasmowych (takich jak SSB, CW, SSTV, PSK itp.) oraz szerokopasmowych transmisji cyfrowej telewizji amatorskich. Transponder wąskopasmowy przekazuje pasmo 2400,0MHz do 24000,3MHz, do dyspozycji radioamatorów jest około 250kHz, czyli tylko nieco mniej ile w paśmie 80m (3,5MHz-3,8MHz), umożliwia więc równoczesną pracę wielu stacji.

![footprint](/assets/images/phocagallery/2019-03-28-EsHail/footprint.jpg)

Jak wspomniano uplink (czyli częstotliwość na której satelita odbiera) to okolice 2,4GHz, natomiast downlink (częstotliwość nadawcza satelity) leży w paśmie 10,48955GHz-10,4898GHz (Tnx SP5MG). Dla radioamatora nie mającego doświadczenia mikrofalowego może to brzmieć odstraszająco, niemniej jednak odbiór jak i nadawanie nie jest bardzo skomplikowane i nie wymaga dużych nakładów finansowych ani sprzętowych.
 Do odbioru satelity wystarczy zwyczajna antena satelitarna o niewielkich rozmiarach wraz z normalnym konwerterem LNB oraz najprostszy odbiornik SDR  (np. RTL-SDR), bądź odbiornik mogący odbierać częstotliwości około 739MHz (10489MHz-9750MHz). Przydają się konwertery LNB z syntezą częstotliwości w celu zapewnienia lepszej stabilności częstotliwości odbieranego sygnału. Można również odbierać satelitę za pomocą [odbiorników Web-SDR](https://eshail.batc.org.uk/nb/).

 Strona nadawcza, pomimo relatywnie dużo niższej częstotliwości stanowi większe wyzwanie, gdyż praktycznie (przynajmniej na razie) brak gotowych kompletnych urządzeń nadawczo-odbiorczych radioamatorskich na to pasmo. Szybko jednak na rynku pojawiły się konwertery podłączane do nadajników pracujących na paśmie 2m/70cm (np. [https://shop.kuhne-electronic.com](https://shop.kuhne-electronic.com/kuhne/en/onlineshop/Hailsat/), [www.dxpatrol.pt](http://www.dxpatrol.pt/index.php/kits)), można też do generacji sygnału 2,4GHz wykorzystać nadajniki SDR takie jak np. Adalm-Pluto, USRP itp. Na ogół na wyjściu konwertera /nadajnika SDR uzyskana moc nie jest wystarczająca (kilka – kilkaset miliwat), wymaga więc wzmocnienia. Tutaj z powodzeniem można użyć wzmacniaczy przeznaczone do sieci Wi-Fi o deklarowanej mocy 2W-8W. Wymagają one na ogół niewielkich modyfikacji i usprawnień a można je nabyć bez większych problemów za niewielkie pieniądze. Jak pokazuje praktyka moc 2W jest już w zupełności wystarczające do uzyskaniu dobrych wyników na SSB. Jako antenę nadawczą najlepiej również wykorzystać zwierciadło paraboliczne (antenę satelitarną) z oświetlaczem pracującym w polaryzacji lewoskrętnej (po odbiciu od zwierciadła sygnał zmienia polaryzację a satelita odbiera sygnały w polaryzacji prawoskrętnej).  Oświetlacz taki z łatwością można wykonać samemu, można też kupić jeden z dostępnych konstrukcji. Istnieją rozwiązania oświetlacza/konwertera w jednej obudowie umożliwiające wykorzystania jednej anteny, w innym wypadku trzeba stosować oddzielną antenę nadawczą i odbiorczą.
 Qatar-Oscar 100 jako jedyny satelita amatorski umożliwia pewną i ciągłą łączność z blisko połową globu i wbrew pozorom stanowić więc może nie tylko ciekawostkę ale i zapewniać komunikację awaryjną. Pojawienie się satelity spowodowało również zwiększenie zainteresowania pasmem 13-cm.
 
W ramach prób i przygotowań do łączności przez satelitę Es’hail 2 w modulacji SSB zostały poczynione przez członków klubu eksperymenty.
 
Do generacji sygnału SSB użyty został transceiver SDR Adalm-Pluto oraz oprogramowanie GnuRadioCompanion . Dzięki zastosowaniu technologii SDR możliwe jest dowolne formowanie sygnału nadajnika i uzyskanie praktycznie dowolnej modulacji poprzez zmiany programowe. Adalm Pluto to budżetowy odbiornik / nadajnik SDR zaprojektowany i wykonany przez Analog Devices zdolny do nadawania i odbioru w paśmie 70MHz – 6GHz. Wadą tego transcivera jest jego bardzo niska moc wyjściowa (rzędu +4dBm=2,5mW) oraz brak filtrów wyjściowych. Moc ta jest nie wystarczająca ani do łączności fonicznej z satelitą, ani do wysterowania wzmacniacza WiFi o mocy wyjściowej 2W. Konieczne jest więc zastosowanie dodatkowego wzmacniacza oraz filtrów. Można pokusić się o zastosowanie któregoś z popularnych wzmacniaczy szerokopasmowych (np. PGA103+ lub podobnych), lub jak w tym wypadku użyć wzmacniacza projektowanego do kart WiFi.
 
Do konstrukcji wzmacniacza posłużyła stara karta WiFi. Dojrzały wiek konstrukcji karty jest jej zaletą, gdyż do jej budowy zostały użyte większe i o mniejszej skali integracji elementy niż w nowocześniejszych rozwiązaniach, niemniej jednak możliwe jest dokonanie podobnych modyfikacji w nowocześniejszych urządzeniach. W omawianej karcie jako wzmacniacz wyjściowy w.cz. zastosowany został układ HFA3983. Umożliwia on uzyskanie mocy wyjściowej rzędu 18dBm (63mW), dodatkowo mamy do dyspozycji cały tor nadawczy oraz filtry. Modyfikacja karty polega na usunięciu większości elementów aktywnych i pozostawienie wyłącznie wzmacniacza w.cz. Należy również usunąć układ przełączający odbiornik i nadajnik i w jego miejsce wstawić zworkę, oraz dolutować kabelek z gniazdem do źródła sygnału oraz podać napięcie na pin 3 układu. Modyfikacje pokazane zostały na zdjęciach poniżej.

![phoca_thumb_l_modyf_przed1](/assets/images/phocagallery/2019-03-28-EsHail/thumbs/phoca_thumb_l_modyf_przed1.jpg)
 
Wyjście tak zmodyfikowanej karty sieciowej zostało podłączone do nieco zmodyfikowanego wzmacniacza WiFi wykonanego w oparciu o dwa układy YP242034 zakupionego przez chiński portal za około 20 dolarów. Wzmacniacz ten powinien dawać wedle deklaracji sprzedawcy (i danych technicznych układów scalonych) 4W, lecz przy sterowaniu z około 65mW udało się uzyskać jedynie około 1W mocy wyjściowej – być może dalsze modyfikacje pozwolą uzyskać większą moc.

![phoca_thumb_l_wzm_wifi](/assets/images/phocagallery/2019-03-28-EsHail/thumbs/phoca_thumb_l_wzm_wifi.jpg)
 
Jako oświetlacz paraboli wykonana została antena spiralna (heilkalna) obliczona przy pomocy [kalkulatora on-line](http://jcoppens.com/ant/helix/calc.en.php). Założono częstotliwość 2,4GHz oraz 5 zwojów. Po wykonaniu anteny okazało się, że minimalny SWR ma ona jednak na częstotliwości 2,5GHz, niemniej jednak SWR na 2,4GHz jest akceptowalny (<2). Jako zwierciadło paraboliczne zastosowano antenę satelitarną offsetową o średnicy około 1m. Po dokładnym naprowadzeniu anteny na satelitę na wykresie waterfall odbiornika pojawił się sygnał z własnej stacji o sile około 10dB ponad poziom tła. Czytelność sygnału bardzo dobra i śmiało można by prowadzić korespondencję.

![phoca_thumb_l_oswietlacz](/assets/images/phocagallery/2019-03-28-EsHail/thumbs/phoca_thumb_l_oswietlacz.jpg)

 ![antena](/assets/images/phocagallery/2019-03-28-EsHail/antena.jpg)
 
Koleją próbą było sprawdzenie czytelności sygnału nadawanego przy pomocy tylko pierwszego stopnia wzmacniacza w.cz., czyli zmodyfikowanej karty sieciowej. Okazuje się, że już 65mW oraz antena o średnicy około 1m wystarczy by przy odrobinie samozaparcia robić łączności foniczne, a z pewnością wystarczyło by do modulacji CW czy PSK. Sygnał odebrany z satelity był silnie zaszumiony, jednak czytelny (jego czytelność można określić na 3-4).

[Sygnał modulujący nadajnik](/assets/audio/Es_hail_org.mp3)

[Sygnał nadawany z mocą około 1W odebrany z satelity](/assets/audio/Es_hail_1W.mp3)

[Sygnał nadawany z mocą około 65mW odebrany z satelity](/assets/audio/Es_hail_65mW.mp3)

Próby zostały wykonane w konfiguracji eksperymentalnej by sprawdzić możliwości nawiązania łączności. W ramach dalszych przygotowań trzeba będzie między innymi usprawnić wzmacniacz końcowy. Wzmacniacz ten powinien oddawać znacznie większą moc – wbudowana w niego przetwornica DC-DC 6V nie jest wystarczająco wydajna prądowo, co z pewnością jest jedną z przyczyn słabych parametrów. Wzmacniacz wykonany z karty sieciowej również powinien oddawać większą moc by w pełni wysterowywać następny stopień. Dla wygody również dobrze było by wykonać upconverter, tak by móc korzystać z radiotelefonu SSB z pasma 70cm.
 
Pierwsze eksperymenty wykazują, iż stosunkowo niewielkim nakładem środków, wykorzystując często sprzęt demobilowy można próbować nawiązywać łączności z tym interesującym satelitą.
