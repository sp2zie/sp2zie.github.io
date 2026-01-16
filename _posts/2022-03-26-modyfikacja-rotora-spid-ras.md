---
layout: post
title: Modyfikacja rotora SPID RAS
date: 2022-03-26
author: Jędrzej Marsz, SQ2DK
category: projekty
---

Koło Naukowe Morski Klub Łączności SZKUNER SP2ZIE przygotowując się do realizacji projektu w zakresie budowy naziemnej stacji do łączności sateli-tarnej na potrzeby komunikacji ze studenckim satelitą PW-Sat3, budowanym przez studentów Politechniki Warszawskiej, podjęło prace zmierzające do po-prawy dokładności pozycjonowania anten wykorzystywanych do śledzenia i nawiązywania łączności z obiektami znajdującymi się w przestrzeni kosmicznej, które przelatują nad terenem Polski. Jednocześnie uznano, za konieczne wyeli-minowanie możliwych błędów pojawiających się w urządzeniach pozycjonują-cych anteny (rotor), celem poprawienia ich niezawodności, która jest nieodzow-na dla zapewnienia stałej i bezpośredniej łączności z obiektem orbitującym w przestrzeni kosmicznej w projektowanej, zdalnie sterowanej stacji naziemnej.

Opisywana tu modyfikacja polega na dodaniu enkodera bezwzględnego azymutu.

Rotory SPID RAS są szeroko stosowanymi i cenionymi rotorami Azymut-Elewacja, używanymi głównie dla amatorskiej łączności radiowej. Najczęściej stosuje się je wraz z stosunkowo lekkimi antenami kierunkowymi na pasmo 2m oraz 70cm. Wszelkie szczegóły dotyczące tego modelu znaleźć można na [stronie producenta](http://spid.net.pl/pl/ras/).

Rotor jest dość niezawodny i zapewnia wystarczającą precyzję do pracy w paśmie 2m i 70cm. Najczęściej jako sterownik do owych rotorów wykorzystuje się sterownik SPID ROT2Prog.

Obrót anteny odbywa się poprzez podanie napięcia na złącza silnika szczotkowego prądu stałego a zwrotnie podawane są impulsy z kontaktronu, który przełączany jest magnesem umieszczonym na tarczy pierwszego stopnia przekładni. W wersji podstawowej otrzymujemy sprzęt, który generuje jeden impuls na stopień.

Rozwiązanie jest to bardzo proste i dość dokładne, posiada jednak wadę związaną z zastosowaniem enkodera inkrementalnego – w przypadku straty impulsu, lub rozprogramowania się sterownika, pozycja rotora będzie obaczona nieznanym błędem, który trzeba skalibrować przez fizyczne sprawdzenie położenia rotora.

Aby wyeliminować tą wadę można dołożyć enkoder bezwzględny, który podaje kąt pod którym ustawiony jest rotor niezależnie od impulsów lub sterownika czy zasilania.

Najprymitywniejszym rozwiązaniem było by dołożenie potencjometru w osi obrotu i sprawdzanie napięcia. Rozwiązanie takie stosuje się w niektórych rotorach. Obecnie na rynku dostępne są enkodery magnetyczne, które nie wymagają mechanicznego sprzężenia osi obrotu z enkoderem i zapewniają doskonałą rozdzielczość i precyzję. W opisywanym rozwiązaniu użyto [enkoder AS5600](https://ams.com/en/as5600) wraz z magnesem neodymowym (uwaga na stosowany magnes – nie we wszystkich zestawach sprzedawane są odpowiednie – wymagany jest taki, gdzie bieguny znajdują się po bokach a nie w orientacji góra-dół). Układ na płytce PCB można kupić za mniej niż 30zł.

 

Modyfikacja polega na rozebraniu górnej części rotora, w celu dostania się do osi obrotu rotora. Trzeba zatem usunąć górną i boczną obudowę rotora oraz odkręcić i zdjąć pierścienie pozycjonujące uchwyt rury elewacji. Warto zaznaczyć położenie wszystkich elementów pisakiem.

![IMG20220321085208](/assets/images/phocagallery/Modyfikacja_RAS/IMG20220321085208.jpg)
 
![IMG20220321091048](/assets/images/phocagallery/Modyfikacja_RAS/IMG20220321091048.jpg)


Następnie należy odkręcić blaszkę przełącznika krańcowego i delikatni wybić rurę elewacji w kierunku ślimacznicy. Należy z wyczuciem wybijać rurę młotkiem przez klocek drewniany. Rura osadzona jest w dwu łożyskach – jest możliwość, że wraz z rurą wysunie się jedno, bądź oba łożyska.

![IMG20220321091435](/assets/images/phocagallery/Modyfikacja_RAS/IMG20220321091435.jpg)

![IMG20220321091650](/assets/images/phocagallery/Modyfikacja_RAS/IMG20220321091650.jpg)

Po usunięciu rury elewacji (wraz z ślimacznicą) otrzymujemy dostęp do końcówki rury azymutu. Kolejnym krokiem jest przygotowanie blachy, która będzie służyła do mocowania enkodera nad osią obrotu w azymucie. W wykonanej modyfikacji zastosowano blachę aluminiową o grubości 2mm. Została ona wycięta w taki sposób, by nie kolidowała z konstrukcją rotora oraz umożliwiała jej solidne przymocowanie do konstrukcji. Do mocowania wykorzystano śrubę M8 przełożoną przez jeden z dostępnych otworów oraz dwie śruby M4 przykręcane do wykonanych w tym celu w konstrukcji nagwintowanych otworów.

![IMG20220321101116](/assets/images/phocagallery/Modyfikacja_RAS/IMG20220321101116.jpg)

![IMG20220321101151](/assets/images/phocagallery/Modyfikacja_RAS/IMG20220321101151.jpg)

![IMG20220321185101](/assets/images/phocagallery/Modyfikacja_RAS/IMG20220321185101.jpg)
 
Pozycję montażu enkodera można ustalić przez zaznaczenie środka osi obrotu na przygotowanej blasze od spodu rotora. Na tym etapie wymagana jest jak największa precyzja, gdyż zamontowanie układu scalonego enkodera dokładnie w osi, będzie wpływała na precyzję pomiaru. Kolejnym krokiem jest zamontowanie płytki PCB enkodera dokładnie, tak by środek układu scalonego znalazł się dokładnie w osi obrotu. Płytkę PCB zamontowano za pomocą czterech śrub M3. W wyznaczonej osi w blasze należy wywiercić otwór (~13mm) a płytkę PCB zamontować układem scalonym do dołu (tak, by widoczny był przez wykonany otwór). Należy zastosować dystanse (nakrętki), tak, by obwód drukowany nie dotykał blachy.

![IMG20220322115948](/assets/images/phocagallery/Modyfikacja_RAS/IMG20220322115948.jpg)

![IMG20220322121120](/assets/images/phocagallery/Modyfikacja_RAS/IMG20220322121120.jpg)

![IMG20220322134016](/assets/images/phocagallery/Modyfikacja_RAS/IMG20220322134016.jpg)

Zastosowany magnes neodymowy ma średnicę 6mm, konieczne więc było wykonanie wałka z materiału niemagnetycznego (aluminium, plastik), tak by móc umieścić magnes w końcówce osi azymutu na odpowiedniej wysokości pod płytką PCB (1-3mm). W wykonanej modyfikacji zarówno magnes, jak i sam wałek zostały wklejone przy użyciu kleju dwuskładnikowego dla pewniejszego uchwytu.

![IMG20220322204710a](/assets/images/phocagallery/Modyfikacja_RAS/IMG20220322204710a.jpg)

![IMG20220324111314](/assets/images/phocagallery/Modyfikacja_RAS/IMG20220324111314.jpg)
 
Do płytki PCB należy przylutować przewód czterożyłowy i podłączyć do niego linie GND, VCC, SCL oraz SDA (dla komunikacji I2C). Przewód można przełożyć przez otwór montażowy którym przechodzą przewody do przełączników krańcowych.

![IMG20220324121838](/assets/images/phocagallery/Modyfikacja_RAS/IMG20220324121838.jpg)

Po zmontowaniu magnesu oraz płytki oraz blachy, rotor należy złożyć w kolejności odwrotnej do procesu rozkładania zachowując wzajemną orientację elementów.

Układ enkodera należy podłączyć do mikrokontrolera, który będzie realizował komunikację używając I2C z enkoderem oraz obrabiał i przesyłał dalej dane. Do mikrokontrolera można również podłączyć akcelerometr, który podawał będzie dokładny bezwzględną wartość elewacji (jeśli podłączony zostanie do rury elewacji). Dla testów wykorzystany został mikrokontroler STM32 blue-pill na który wgrano prosty program napisany w środowisku Arduino.

Po podłączeniu do sterownika Rot2Prog rotor było obracany o 10 stopni i wyniki odczytane ze sterownika oraz enkodera porównane (obrót jedną stronę). Wykres błędu enkodera przedstawiono poniżej.

![err graph](/assets/images/phocagallery/Modyfikacja_RAS/err_graph.png)

Błędy wynikają z nieprecyzyjnego umieszczenia enkodera w stosunku do osi obrotu.

Zebrane informacje o błędach zostały dodane do programu odczytu kąta, gdzie następuje ich automatyczna korekta. Po tym zabiegu dokładność odczytu kąta azymutu wynosi +/-0,2 stopnia.

Na tą chwilę program mikrokontrolera nie posiada dużej funkcjonalności i jest w trakcie rozwijania. Należy również zdecydować się na protokół transmisji tak w warstwie sprzętowej, jak i programowej.

Zastosowanie enkodera bezwzględnego nie tylko może podnieść niezawodność rotora, ale również może zwiększyć dokładność odczytu kąta. Pozwoli też zastosować inny, niż fabryczny sterownik, jeśli opracowany zostanie stosowny protokół komunikacyjny.
