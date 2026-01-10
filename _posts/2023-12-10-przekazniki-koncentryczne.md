---
layout: post
title: Przekaźniki koncentryczne
date: 2023-12-10
author: Jędrzej Marsz, SQ2DK
categories: 
  - Projekty techniczne
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

<table border="1" style="width: 100%;" cellpadding="0" cellspacing="0"><colgroup> <col width="43*" /> <col width="43*" /> <col width="43*" /> <col width="43*" /> <col width="43*" /> <col width="43*" /> </colgroup>
<tbody>
<tr valign="top">
<td style="border: medium; padding: 0cm; width: 17%;">
<p>&nbsp;</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>CX-140D</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>CX-600N</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>565-413-000</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>R570-4621-00</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>919C70100</p>
</td>
</tr>
<tr valign="top">
<td style="border: medium; padding: 0cm; width: 17%;">
<p>Złącza</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>N / brak</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>N</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>SMA</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>SMA</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>SMA</p>
</td>
</tr>
<tr valign="top">
<td style="border: medium; padding: 0cm; width: 17%;">
<p>Napięcie cewki</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>12V</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>12V</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>26V</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>12V / TTL</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>26V</p>
</td>
</tr>
<tr valign="top">
<td style="border: medium; padding: 0cm; width: 17%;">
<p>Max moc</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>200W</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>800W</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>200W</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>200W</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>50W</p>
</td>
</tr>
<tr valign="top">
<td style="border: medium; padding: 0cm; width: 17%;">
<p>Tłumienie</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>0,2dB</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>0,3dB</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>&lt;0,1dB</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>&lt;0,1dB</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>&lt;0,1dB</p>
</td>
</tr>
<tr valign="top">
<td style="border: medium; padding: 0cm; width: 17%;">
<p>Izolacja</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>32,5dB</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>40dB</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>110dB</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>&gt;80dB</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>&gt;80dB</p>
</td>
</tr>
<tr valign="top">
<td style="border: medium; padding: 0cm; width: 17%;">
<p>Czas załączania</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>13ms</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>26ms</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>7ms</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>3ms</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>7,3ms</p>
</td>
</tr>
<tr valign="top">
<td style="border: medium; padding: 0cm; width: 17%;">
<p>Czas rozłączania</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>9ms</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>17ms</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>6ms</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>3ms</p>
</td>
<td style="border: medium; padding: 0cm; width: 17%;">
<p>4ms</p>
</td>
</tr>
</tbody>
</table>


Poza przekaźnikiem CX-140D, gdzie zmierzona izolacja jest znacznie gorsza o przeszło 10dB gorsza od deklarowanej przez producenta parametry w większości pokrywają się z parametrami deklarowanymi przez producentów. Widać tu wyraźną różnicę w jakości przekaźników przeznaczonych na rynek profesjonalny i wojskowy w stosunku do przekaźników przeznaczonych głównie na rynek amatorski (Tohtsu).

Z racji dość kiepskich parametrów izolacji oraz dość długiego czasu komutacji do budowy stacji, gdzie to możliwe wykorzystane będą demobilowe przekaźniki z rynku profesjonalnego. Planuje się wykorzystanie przekaźnika CX-140, ale dla uzyskania dostatecznej separacji będzie zastosowany w parze z cyrkulatorem.

Na podstawie maksymalnego czasu komutacji (przełączania) trzeba ustawić czas opóźnienia nadawania w sekwencerze na co najmniej 15ms.
