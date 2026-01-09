---
layout: post
title: Planowany odbiór ARISS TV – odsłona II
date: 2015-11-04
author: Dariusz Mankiewicz, SP2HQY
categories: 
  - Amateur Radio on the ISS (ARISS)
---

Po wykonaniu oświetlacza i zamontowaniu go na antenie offsetowej postanowiliśmy rozpocząć próby odbioru sygnałów w paśmie dedykowanym dla ARISS HamTV , czyli w paśmie 2,4 GHz. W tym celu antenę wyposażyliśmy w konwerter BT-480 produkcji Anhui Bowei Electronics Technology Co. Ltd., a następnie przenieśliśmy czaszę naszej anteny na nieduży maszt kratowy wraz z rotorem Az-El.

Nowa lokalizacja anteny stała się pewnym wyzwaniem z uwagi na konieczność kalibracji sterownika. Trzeba bowiem pamiętać, że użyta przez nas antena nie patrzy wprost na obiekt (satelitę), lecz jako antena offsetowa jest dodatkowo nachylona pod kątem, który musi zostać uwzględniony przy określaniu współrzędnych położenia anteny. Na szczęście mamy w naszych szeregach doświadczonego nawigatora, który szybko poradził sobie z tym problemem wykorzystując swoje umiejętności (Vy Tnx Jędrzej).

Z racji braku źródła sygnału w paśmie 13cm w znanej lokalizacji, który moglibyśmy odebrać naszym zestawem, powstała przenośna „radiolatarnia" skompilowana z chińskiego klonu NWT-4000 (generator/"analizator widma" - BG7TBL - 138MHz-4,4GHz), sterujący nim Arduino uno z naprędce napisanym programem kluczującym CW, baterii żelowej oraz anteny. Moc wyjściowa generatora to około 0,5mW.

Dzięki uprzejmości Kolegi Michała SP2IQW w jego radioshacku (czytaj na jego dachu) umieściliśmy wyżej wspomnianą radiolatarnię.

Pierwsze próby odbioru sygnałów testowych generowanych z lokalizacji Kolegi Michała SP2IQW, przyniosły całkiem przyzwoite wyniki. Do pomiaru poziomu szumu używaliśmy karty DVB-S TechniSat Skystar HD (odpowiednik Technotrend TT-Budget S2-3200) a do odbioru „telegrafii" odbiornika SDR RTL2823Uwraz z programem SDR-Sharp. Po skierowaniu anteny na źródło sygnału na spektrogramie wyraźnie można było zidentyfikować sygnał.

Sprawdzaliśmy również odbiór z wykorzystaniem przerobionych konwerterów MMDS (Multichannel Multipoint Distribution Service)

Pierwsze próby napawają optymizmem, choć mamy już pewne przemyślenia na temat potencjalnych ulepszeń, ale o tym po próbach odbioru sygnałów ARISS HamTV.

{% include image-gallery.html folder="assets/images/phocagallery/20151003-ARISS-HamTV-cz2/thumbs" %}
