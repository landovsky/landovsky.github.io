---
layout: post
title:  "Spotřeba fosilních paliv jako zdrojů energie v ČR"
date:   2022-11-05 21:15:34 +0100
categories: energie update
---
### WIP: Jaká je spotřeba energií v ČR?

Chtěl jsem si udělat představu o energetických požadavcích České Republiky. Mluví se o stavbě dalšího bloku Temelínu, o nahrazování špinavých zdrojů těmi obnovitelnými. Energii spotřebováváme ale i jinak než ve formě elektřiny. Kdybychom měli nahradit opravdu veškeré fosilní zdroje, o jaké množství energie by se jednalo?

Nejblíže k nástinu měl článek portálu [oenergetice.cz][clanek-o-energetice], který se ale dívá na globální spotřebu. Pohled na spotřebu z hlediska ČR mi přijde představitelnější než pohled globální.

Předpokládaný postup:
1. Najít zdroje dat o spotřebě fosilních paliv
2. Převést je na společné jednotky TWh
3. Porovnat s jednotkou výroby

### Zdroje
Jako zdroj poslouží stránka ČSÚ [Spotřeba paliv a energie](https://www.czso.cz/csu/czso/spotreba-paliv-a-energie), kde najdeme spotřebu jednotlivých typů paliv.
Již při hledání zdrojů jsem si vybral rok 2020 pro který by již mohla být dostupná data a proto jsem zvolil z katalogu ČSÚ tento rok.

Katalog obsahuje spotřebu paliv a el. energie dle odvětví. U každého typu paliva jsou uvedené jednotky objemu (tuny, litry) a GJ jako jednotka energie.

Některá odvětví mohou používat fosilní zdroje jinak než paliva, např. na výrobu léků. Očištění o tato odvětví jsem neprovedl, protože

[clanek-o-energetice]: https://oenergetice.cz/zahranicni/iea-fosilni-paliva-mela-2017-podil-813-celosvetove-produkci-energie