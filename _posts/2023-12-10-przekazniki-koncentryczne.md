---
layout: page
title: Przekaźniki koncentryczne
date: 2023-12-10
author: Jędrzej Marsz, SQ2DK
category: projekty
subcategory: pw-sat3
---

W praktyce radiowej często zachodzi potrzeba przełączania sygnałów wysokiej częstotliwości. O ile dla sygnałów o niewielkiej amplitudzie można bez trudu to zadanie realizować za pomocą układów elektronicznych (scalone przełączniki w.cz., diody pin itp.) o tyle w wypadku przełączania nadawanie-odbiór, gdzie przełączane sygnały mogą się różnić o nawet 200dB trudno to wykonać w oparciu o przełączniki elektroniczne. W takich przypadkach często stosuje się przekaźniki mechaniczne, gdzie za pomocą elektromagnesu przełączane są styki mechaniczne. Dla stosunkowo niewielkich częstotliwości można stosować tradycyjne przekaźniki, dla wysokich częstotliwości nie zdają one jednak egzaminu. Dla przekaźnika pracującego z sygnałami wysokiej częstotliwości należy wsiąść pod uwagę kilka parametrów a wśród nich: impedancję falową (Zo), tłumienie przenoszenia (Ap), izolacje między portami (tłumienie przesłuchu) (Ai) oraz maksymalną przenoszoną moc dla określonej częstotliwości (Pmax). Z dodatkowych parametrów można wymienić: rodzaj zastosowanych złącz w.cz., napięcie i prąd cewki oraz szybkość przełączania.

![przekazniki](/assets/images/phocagallery/2023_12_PW_sat3/przekazniki.jpg)

W ramach przygotowań do budowy satelitarnej stacji naziemnej zdecydowano się na wykorzystanie przekaźników koncentrycznych do realizacji przełączania torów odbiorczego i nadawczego. Wykonano pomiary dostępnych przekaźników pod względem: tłumienia w paśmie przepustowym, izolacji oraz prędkości przełączania by dobrać najstosowniejsze odpowiednie przekaźniki do stawianych im zadań.

Pomiary zostały wykonane dla następujących modeli przekaźników:

[Tohtsu CX-140D](https://www.wimo.com/media/akeneo_connector/media_files/3/1/31102_CX_140D_V1_2023_04_27_EN_4913.pdf)

[Tohtsu CX-600N](https://www.wimo.com/media/akeneo_connector/media_files/3/1/31108_CX_600N_V1_2023_04_27_EN_51ec.pdf)

[Radiall R 565-413-000](https://www.limpulsion.fr/upload/docs/R565_R555.PDF)

[Radiall R570-4621-00](https://www.mouser.pl/datasheet/2/516/R570462100-2502305.pdf)

[Transco / Dow-Key 919C70100](http://f1chf.free.fr/fichiers/datasheet%20relais/DowKeyCatalogue.pdf)

Wyniki przedstawiono w poniższej tabeli - podane wartości dla pasma 70cm:

<table class="table table-bordered table-striped table-hover">
<thead>
<tr>
<th></th>
<th>CX-140D</th>
<th>CX-600N</th>
<th>565-413-000</th>
<th>R570-4621-00</th>
<th>919C70100</th>
</tr>
</thead>
<tbody>
<tr>
<td>Złącza</td>
<td>N / brak</td>
<td>N</td>
<td>SMA</td>
<td>SMA</td>
<td>SMA</td>
</tr>
<tr>
<td>Napięcie cewki</td>
<td>12V</td>
<td>12V</td>
<td>26V</td>
<td>12V / TTL</td>
<td>26V</td>
</tr>
<tr>
<td>Max moc</td>
<td>200W</td>
<td>800W</td>
<td>200W</td>
<td>200W</td>
<td>50W</td>
</tr>
<tr>
<td>Tłumienie</td>
<td>0,2dB</td>
<td>0,3dB</td>
<td>&lt;0,1dB</td>
<td>&lt;0,1dB</td>
<td>&lt;0,1dB</td>
</tr>
<tr>
<td>Izolacja</td>
<td>32,5dB</td>
<td>40dB</td>
<td>110dB</td>
<td>&gt;80dB</td>
<td>&gt;80dB</td>
</tr>
<tr>
<td>Czas załączania</td>
<td>13ms</td>
<td>26ms</td>
<td>7ms</td>
<td>3ms</td>
<td>7,3ms</td>
</tr>
<tr>
<td>Czas rozłączania</td>
<td>9ms</td>
<td>17ms</td>
<td>6ms</td>
<td>3ms</td>
<td>4ms</td>
</tr>
</tbody>
</table>

Poza przekaźnikiem CX-140D, gdzie zmierzona izolacja jest znacznie gorsza o przeszło 10dB gorsza od deklarowanej przez producenta parametry w większości pokrywają się z parametrami deklarowanymi przez producentów. Widać tu wyraźną różnicę w jakości przekaźników przeznaczonych na rynek profesjonalny i wojskowy w stosunku do przekaźników przeznaczonych głównie na rynek amatorski (Tohtsu).

Z racji dość kiepskich parametrów izolacji oraz dość długiego czasu komutacji do budowy stacji, gdzie to możliwe wykorzystane będą demobilowe przekaźniki z rynku profesjonalnego. Planuje się wykorzystanie przekaźnika CX-140, ale dla uzyskania dostatecznej separacji będzie zastosowany w parze z cyrkulatorem.

Na podstawie maksymalnego czasu komutacji (przełączania) trzeba ustawić czas opóźnienia nadawania w sekwencerze na co najmniej 15ms.
