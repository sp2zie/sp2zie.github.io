---
layout: post
title: Krótko o technicznych aspektach związanych z AIS
date: 2011-03-18
author: Jędrzej Marsz, SQ2DK
category: projekty
---

Obecnie prawie wszystkie statki morskie wyposażane są zgodnie z konwencją o bezpieczeństwie na morzu w transponder AIS. AIS jest to system automatycznej identyfikacji statków – Automatic Identyfication System. Pozwala on statkom oraz stacjom brzegowym wyposażonym w podobne transpondery na nadawanie własnej pozycji oraz parametrów ruchu oraz odbiór takich informacji nadawanych przez inne jednostki. Głównym zadaniem systemu jest poprawa bezpieczeństwa (w rozumieniu safety i security) żeglugi, poprzez umożliwienie monitorowanie ruchu na akwenie wraz z jednoznaczną identyfikacją jednostek.

Jako medium dla przekazywania informacji wybrano wycinek radiowego pasma morskiego UKF a dokładniej dwa kanały 87B oraz 88B (161,975MHz oraz 162,025MHz). W związku z wybraniem takiej częstotliwości system ma szereg ograniczeń (które świadomie uwzględniono).

Pierwszą z nich jest ograniczony zasięg – sygnały wysłane mogą zostać odebrane praktycznie w zasięgu optycznym – czyli dla przeciętnej jednostki pływającej w promieniu około 40km. Zasięg ten wynikający z ograniczeń propagacyjnych pasma ultrakrótkofalowego zależny jest przede wszystkim od wysokości instalacji anteny nadawczej i odbiorczej, oraz w mniejszym stopniu od mocy nadajnika i innych czynników.

Kolejnym ograniczeniem jest prędkość transmisji ograniczony szerokością kanału radiowego wynoszącego 25kHz. Zdecydowano się użyć najwyższą możliwą w tych warunkach prędkość wynoszącą 9600 bodów. Konsekwencją tego było również zastosowanie modulacji GMSK. Aby z jednego bądź dwu kanałów mogło skorzystać wiele stacji zastosowano podział czasowy (Time Division Multiply Access - TDMA). Stacje wysyłają pakiety o długości 256 bitów, w związku z czym łatwo wyliczyć, iż w minutę można wysłać (60[s]*9600[bd])/256[bit]=2250. Na uwagę zasługuje również sposób synchronizacji danych – aby uniknąć kolizji ramek (dwie stacje nadające swoje dane w tym samym czasie) zastosowano synchronizacje. Na ogół w podobnych systemach ruchem zawiaduje pewna stacja „nadrzędna” przyznająca ramki czasowe. Z uwagi na fakt, iż w warunkach morskich, gdzie system musi działać równie dobrze na otwartym morzu gdzie nie może być żadnych stacji nadrzędnych, zdecydowano się na organizację w oparciu o bardzo dokładny wzorzec czasu jakim jest GPS. Każda ze stacji zajmuje wolną szczelinę czasowa (bądź w wypadku braku wolnych szczelin, szczelinę stacji najodleglejszej), a ponieważ wszystkie stacje korzystają ze wspólnego źródła czasowego system jest zsynchronizowany. Taką odmianę TDMA nazwano samoorganizującym się TDMA czyli SOTDMA (Self Organized Time Division Multiple Accsess).

Z 256 bitów składających się na pojedynczą ramkę tylko 128 bitów przekazuje istotna informację (pozostałe to bity synchronizacyjne i bufory). Jak więc można się przekonać w pojedynczej ramce można przekazać niewiele informacji, mimo wszystko jest ich zadziwiająco wiele. Częstość nadawania danych zależy od statusu oraz prędkości jednostki i tak jednostka zacumowana lub na kotwicy nadaje informacje o pozycji co około 3 minuty, podczas gdy statki płynące w zależności od prędkości i zmian kursu nadają pozycje co 1 do 12 sekund. Niektóre informacje takie jak pozycja, kurs, prędkość są bardziej istotne od innych (takich jak port docelowy oraz nazwa), w związku z czym nadawane są częściej.

Dla stacji na statkach można rozróżnić dwie podstawowe ramki zawierające odpowiednie dane na temat:

Ramka typu 1

* numer MMSI – unikalny numer „wywoławczy” jednostki
* status nawigacyjny (16 zdefiniowanych statusów taki jak np. „na kotwicy”, „zacumowany” itp.)
* szybkość zwrotu (ROT – rate of turn)
* prędkość względem dna (z GPS)
* dokładność pozycji
* długość geograficzna
* szerokość geograficzna
* kąt drogi nad dnem (Z GPS)
* kurs rzeczywisty (z żyrokompasu)
* znacznik czasu

Ramka typu 5

* numer MMSI – unikalny numer „wywoławczy” jednostki
* numer IMO – unikalny numer kadłuba
* znak wywoławczy statku
* nazwa statku
* typ statku oraz ładunku (jeden z predefiniowanych typów)
* rozmiary statku oraz położenie anteny na statku
* przybliżony czas dotarcia do portu przeznaczenia
* aktualne maksymalne zanurzenie
* port przeznaczenia
* inne

Ramka typu 1 nadawana jest z częstością opisaną wyżej, natomiast ramka typu 5 zawierająca informacje statyczne nadawana jest co 6 minut. Ponieważ jak wspomniano wyżej do transmisji używane są dwa kanały częstość występowania każdej z ramek należy podwoić, gdyż nadawane są naprzemiennie to na jednym to na drugim kanale.

Jak widać z powyższego dostępne są dość szczegółowe dane. Część z tych informacji dostępne są z czujników statkowych (GPS, żyrokompas), część informacji, które zmieniają się stosunkowo rzadko – takie jak port przeznaczenia czy zanurzenie wprowadzana jest jednak przez operatora. W tym celu dostępny na statku jest interfejs użytkownika w postaci wyświetlacza z klawiaturą (MKD – Minimum Keyboard Display).


![mkd](/assets/images/phocagallery/sq2dk-sq2dk-4043/mkd.jpg)

Pozostała część urządzenia w postaci skrzynki, anten i kabli wraz z ewentualnymi interfejsami są na ogół schowane. Interfejs użytkownika pozwala również na przeglądania odebranych danych. Ze względu jednak na ograniczenia sprzętowe nie jest to specjalnie wygodne – dużo większą swobodę i łatwość interpretacji danych daje podłączenie transpondera do radaru i mapy elektronicznej. W takim układzie na mapie elektronicznej wyświetlane są symbole jednostek w ich pozycjach i po ich wybraniu można uzyskać szczegółowe dane na ich temat.

![vms](/assets/images/phocagallery/sq2dk-sq2dk-4043/vms.jpg)

Ze względu na fakt użytego medium (fale radiowe z zakresu UKF) oraz otwartości specyfikacji transmisji możliwy jest odbiór AIS w warunkach amatorskich. Do tego celu można wykorzystać dedykowane odbiorniki dostępne w handlu. Odbiorniki takie zawierają w sobie tor radiowy oraz modem GMSK (w wypadku odbiorników dwukanałowych są 2 tory radiowe i dwa modemy). Dane wyjściowe są dostępne w formacie NMEA i aby je wizualizować niezbędny jest komputer ze stosownym oprogramowaniem. Dedykowany odbiornik można zastąpić odbiornikiem radiowym na częstotliwość jednego z kanałów AIS (skaner lub radiotelefon) oraz komputer ze stosownym oprogramowaniem modemu GMSK oraz dalej kolejny program do wizualizacji. Dostępne są również amatorskie serwisy internetowe do których można wysyłać odebrane dane aby udostępnić je wszystkim zainteresowanym. Oczywiście pokrycie powierzchniowe ogranicza się do brzegów (około 30km w głąb morza), tylko w okolicach stacji brzegowych udostępniające takie dane. Jako, iż stacje te są prowadzone amatorsko pokrycie jest niepełne i niepewne. Istnieją również podobne serwisy komercyjne jak i profesjonalne. Dane z tych pierwszych dostępne są dla wszystkich po uiszczeniu opłaty – niektóre z takich serwisów oferują również dane AIS zbierane za pomocą satelitów, które znakomicie powiększają zasięg powierzchni monitorowanej. Serwisy profesjonalne dostępne są wyłącznie dla jednostek administracyjnych oraz uprawnionych. Ponieważ wykorzystują bogatą infrastrukturę pokrywają bardzo dużą powierzchnie oraz mają dużą niezawodność.
