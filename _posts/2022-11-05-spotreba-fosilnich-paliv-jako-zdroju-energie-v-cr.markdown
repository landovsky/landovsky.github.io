---
layout: post
title:  "Spotřeba fosilních paliv jako zdrojů energie v ČR"
date:   2022-11-05 21:15:34 +0100
categories: cz
---
### Jaká je spotřeba energií v ČR?

Chtěl jsem si udělat řádovou představu o energetických požadavcích České Republiky. Mluví se o stavbě dalšího bloku Temelínu, o nahrazování špinavých zdrojů těmi obnovitelnými nebo nízkoemisními. Energii spotřebováváme ale i jinak než ve formě elektřiny. Kdybychom měli nahradit opravdu veškeré fosilní zdroje, o jaké množství energie by se jednalo?

V době, kdy jsem se tímto zabýval měl nejblíže k nástinu článek portálu [oenergetice.cz][clanek-o-energetice]{:target="_blank"}, který se ale dívá na globální spotřebu. Pohled na spotřebu z hlediska ČR mi přijde představitelnější než pohled globální.

Později vyšel [článek na kurzy.cz][kurzy-spotreba-v-cr-2020]{:target="_blank"}, který uvádí spotřebu v PJ (peta joulech) a analyzuje strukturu paliv a energií a její spotřebitele.

Předpokládaný postup:
1. Najít zdroje dat o spotřebě fosilních paliv
2. Převést je na společné jednotky TWh
3. Porovnat s jednotkou výroby

### Zdroj dat
Jako zdroj poslouží stránka ČSÚ [Spotřeba paliv a energie][csu-spotreba-paliv-a-energie]{:target="_blank"}, kde najdeme spotřebu jednotlivých typů paliv.
Již při hledání zdrojů jsem si vybral rok 2020 pro který by již mohla být dostupná data pro všechny typy paliv a proto jsem zvolil z katalogu ČSÚ tento rok.

Katalog obsahuje spotřebu paliv a el. energie dle odvětví. U každého typu paliva jsou uvedené jednotky objemu (tuny, litry) a GJ jako jednotka energie.

Některá odvětví mohou používat fosilní zdroje jinak než spalováním (výrobu tepla, elektřiny, nebo ve spalovacích motorech), např. na farmaceutický nebo chemický průmysl. Očištění o tato odvětví jsem ale neprovedl, protože mi spotřeba mimo spalování nepřišla významná. Jako příklad jsem si vybral největší položku spotřeby zemního plynu - odvětví "Výroba chemických látek a chemických přípravků" spotřebovalo cca 7% plynu, což řádově neovlivní číslo, ke kterému se chci dostat.

Zpětně jsem se podíval na ostatní typy paliv - koks a černé uhlí, kde je situace podobná.

### Převod jednotek
U všech surovin byly uveden ekvivalent v GJ (giga joulech). Protože jsem chtěl vědět, kolik el. energie by muselo být vyprodukováno pro náhradu fosilních paliv, potřeboval jsem GJ převést na TWh (tera-watt hodiny). 1 W = 1 joule / sek., takže když vydělíme GJ 3600, dostaneme GWh a / 1000 TWh.

Elektrickou energii jsem do energetické náročnosti nedával, protože suroviny pro její výrobu jsou v tabulce již započteny a energii z nízkoemisních zdrojů nezapočítáváme, ta už se nízkoemisně vyrábí.

### Výsledky
Z fosilních paliv v ČR spotřebujeme 780 PJ, nebo-li 216 TWh energie.
Číslo je ohromující. Pro představu, je to ekvivalent:
- 14 Temelínů
- 7x všech jaderných zdrojů v ČR
- 21,7 miliónů domácích solárních elektráren (10KWp)

**Celková spotřeba fos. paliv v ČR 2020**

| **Zdroj energie** |     **PJ** |    **TWh** |
|-------------------|-----------:|-----------:|
| hnědé uhlí        |     352.45 |      97.90 |
| zemní plyn        |     177.58 |      49.33 |
| černé uhlí        |     120.11 |      33.36 |
| nafta             |      68.21 |      18.95 |
| koks              |      57.72 |      16.03 |
| benzín            |       4.21 |       1.17 |
| brykety           |       0.01 |       0.00 |
| **Celkem**        | **780.30** | **216.75** |

**Srovnání s výrobou elektřiny**

Na výrobu el. energie bylo použito 38% fos. paliv. 62% (kromě PHM) bylo využito pro výrobu tepla v domácnostech, firmách a průmyslu.

| **Zdroj energie**      | **PJ** | **TWh** |
|------------------------|--------|--------:|
| el. z fosilních zdrojů | -      |      41 |
| el. z ostatních zdrojů | -      |      41 |

[Zdrojová data (Google Sheet)][tabulka-gsheet]{:target="_blank"}

### Závěr
Vzhledem k "rychlosti" elektrifikace si lze těžko představit, že během krátké doby (řekněme 10, nebo 20 let) bude naše spotřeba energií bezemisní. To je určitě složitější téma, protože v něm hraje roli spousta faktorů - snižování energetické náročnosti budov, zlepšování efektivity vytápění, snižování spotřeby vlivem oteplování, atd. To je k zamyšlení na někdy jindy.


[clanek-o-energetice]: https://oenergetice.cz/zahranicni/iea-fosilni-paliva-mela-2017-podil-813-celosvetove-produkci-energie
[vyuziti-plynu-v-prumyslu]: https://www.wingas.cz/fileadmin/Wingas/content/06_Presse_Mediathek/Broschueren/Studies/210924_Wingas_Factsheet_Industrie_EN.pdf
[kurzy-spotreba-v-cr-2020]: https://www.kurzy.cz/zpravy/679785-kolik-plynu-elektriny-ropy-a-dalsich-zdroju-se-spotrebuje-a-na-co/
[vyroba-temelin]: https://trebicsky.denik.cz/zpravy_region/dukovany-a-temelin-hlasi-druhou-nejvyssi-vyrobu-v-historii-20220103.html
[tabulka-gsheet]: https://docs.google.com/spreadsheets/d/1vdNPmwila56Nor2sWxiaqkr0rjtOQumdgzrRP5-TZ4k
[csu-spotreba-paliv-a-energie]: https://www.czso.cz/csu/czso/spotreba-paliv-a-energie