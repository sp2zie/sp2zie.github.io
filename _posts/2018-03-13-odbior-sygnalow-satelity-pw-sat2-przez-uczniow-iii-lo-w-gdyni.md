---
layout: post
title: Odbiór sygnałów satelity PW-SAT2 przez uczniów III LO w Gdyni
date: 2018-03-13
author: Michał Lewczuk, SP2XDM
categories: 
  - Per radio ad astra
---

**Charakterystyka**

  Projekt pod nazwą Per radio ad astra ma na celu umożliwienie młodzieży licealnej kontaktu z techniką kosmiczną poprzez odbiór sygnałów emitowanych przez sztuczne satelity ziemi, ze szczególnym uwzględnieniem obiektów konstruowanych przez polskich studentów w ramach programu PW-Sat. Projekt pozwoli na przygotowanie programu edukacyjnego, rozwiązań technicznych oraz zasad i form współpracy pomiędzy placówkami dydaktycznymi oraz naukowymi, których celem będzie poszerzenie wiedzy o elementach nauki wykorzystywanej w eksploracji kosmosu oraz wzmożenie zainteresowania polską myślą techniczną wykorzystywaną w podboju kosmosu.
Projekt zostanie zrealizowany przy wykorzystaniu środków i kadr Koła Naukowego Morski Klub Łączności SP2ZIE SZKUNER Akademii Morskiej w Gdyni oraz III Liceum Ogólnokształcącego w Gdyni, przy współpracy z Studenckim Kołem Astronautycznym Politechniki Warszawskiej oraz wsparciu Centrum Badań Kosmicznych Polskiej Akademii Nauk.

**Opis projektu**

  W celu realizacji projektu członkowie Koła Naukowego Morski Klub Łączności SP2ZIE SZKUNER Akademii Morskiej w Gdyni wykonają odbiorczą stację naziemna wyposażoną w odpowiednie urządzenia odbiorcze oraz zestawy antenowe umożliwiające odbiór sygnałów pochodzących z przestrzeni kosmicznej z jednoczesnym śledzeniem ruchu obiektów krążących na orbicie okołoziemskiej, a w szczególności polskiego satelity studenckiego PW-Sat2. Wykonana stacja pozwoli na odbiór słabych sygnałów emitowanych przez sztuczne satelity ziemi. Następnie odebrane sygnały zostaną przekazane za pośrednictwem łącza internetowego do III Liceum Ogólnokształcącego w Gdyni, gdzie przy wykorzystaniu odpowiednich narzędzi informatycznych będą prowadzone zajęcia dla uczniów szkół średnich z technik odbioru sygnałów satelitarnych.

**PW-Sat2**

![pwsat](/assets/images/stories/praa/pwsat.png)  

PW-Sat2 jest studenckim projektem edukacyjnym, którego głównym celem technologicznym jest skonstruowanie i przetestowanie innowacyjnego systemu deorbitacji w postaci żagla o powierzchni 4 m². Ponadto przetestowany zostanie system otwieranych paneli słonecznych, czujnik Słońca oraz algorytmy sterowania satelitą. System zasilania, struktura satelity i oprogramowanie misji są autorskimi projektami członków zespołu.
Satelita wyposażony jest w moduł komunikacyjny dzięki któremu możliwa jest bieżąca obserwacja stanu poszczególnych podzespołów poprzez analizę wysyłanych sygnałów (tzw. telemetrii). Ponadto PW-Sat2 wyposażony jest w moduł antenowy składający się z dwóch dipoli półfalowych, które zostaną otworzone tuż po wprowadzeniu satelity na orbitę. Spodziewany poziom odbieranego sygnału na ziemi wynosi ok. -120dBm. Z tego względu do odbioru sygnałów z PW-Sat2 na ziemi niezbędna jest stacja radiowa wyposażona w odpowiednio czułe odbiorniki, jak i zestaw anten umożliwiające odbiór niezwykle słabych sygnałów w paśmie o częstotliwości 435,275 MHz.

![insidepwsat](/assets/images/stories/praa/insidepwsat.jpg)

**Stacja naziemna**

![antennas](/assets/images/stories/praa/antennas.jpg)  

Na terenie Akademii Morskiej w Gdyni, w pomieszczeniach Koła Naukowego Morski Klub Łączności SP2ZIE SZKUNER przy Akademii Morskiej w Gdyni zostanie wykonana naziemna stacja odbiorcza sygnałów satelitarnych. Stacja będzie wyposażona w odbiorniki SDR (software-defined radio, radio definiowane programowo). Odbiorniki SDR zostaną podłączone do komputera, który przy wykorzystaniu dedykowanego oprogramowania zwizualizuje widmo odbieranego sygnału oraz pozwoli na jego przekazanie do III Liceum Ogólnokształcącego w Gdyni przy wykorzystaniu łącza internetowego. Wykorzystanie oprogramowania dedykowanego dla SDR zarówno po stronie stacji odbiorczej, jak i placówki dydaktycznej daje możliwość przesłania pełnego spektrum odbieranego sygnału oraz jego dekodowania (w przypadku udostępnienia odpowiedniego dekodera przez Studenckie Koło Astronautyczne Politechniki Warszawskiej). Należy zwrócić uwagę, że studencki satelita PW-Sat2 będzie nadawał swoje sygnały z mocą nie przekraczającą 500mW, a co za tym idzie odbiór sygnałów o tak niskim poziomie z odległości ponad 500 km (przewidywana orbita 575 km nad powierzchnią ziemi) będzie wymagało użycia odpowiednio czułych odbiorników, przedwzmacniaczy niskoszumowych oraz zestawu antenowego zapewniającego odpowiedni zysk i kierunkowość anten. Istotne jest również, iż satelita będzie orbitował przemieszczając się w czasie misji ponad 600 razy nad terenem Polski. Powyższe wymaga więc śledzenia ruchu satelity w czasie jego przelotu. Z tego względu zostanie użyty zestaw sterujący, który będzie naprowadzał anteny na przelatujący obiekt. Zastosowane rozwiązanie będzie wymagało predykcji przelotów oraz miejsca położenia obiektu ponad horyzontem i korelacji danych o położeniu obiektu z ruchem zestawu naprowadzającego. Dla uzyskania niezbędnej dokładności zostanie użyte odpowiednie oprogramowanie sterujące zestawem naprowadzającym, które zostanie zaimplementowane na potrzeby niniejszego projektu.
