# Hydraulika — průtoky, výšky, tlaky, ztráty

Rozpočet výtlaku obou větví a z něj plynoucí optimalizace. Naměřená čísla jsou z [lab.md](lab.md) (kbelík **5. 9. 2026**), as-built z [zapojeni.md](zapojeni.md), postup u vody v [provoz.md](provoz.md).

**Co je měřené a co spočítané.** Měřené jsou jen dva průtoky (950 a 2 250 l/h) a katalogové štítky. Všechno ostatní v tomto souboru je **dopočet**. Kde chybí data, je to napsané a je u toho test, ne odhad vydávaný za fakt.

---

## Vstupy

| Veličina | Hodnota | Zdroj |
| --- | --- | --- |
| AquaMax Eco Premium 6000 12 V | 6 000 l/h, max. **3,2 m**, 45–55 W | Oase, art. 50730 |
| AquaMax Eco Premium 12000 12 V | 11 400 l/h, max. **3,2 m**, **95 W**, trny 25/32/38/50 | Oase, art. 50382 |
| Sicce Green Reset 100 | 16 000 l/h, **max. 0,4 bar**, trny 32/38/50 | Sicce |
| UV 2× 55 W | trn max. **38 mm** (analog Vitronic) | e-shop |
| INVITAL Biofiltr 550 | 130 l, gravitační výtok | e-shop |
| Naměřeno větev 1 (výtok IBC) | **950 l/h** | kbelík 5. 9. 2026 |
| Naměřeno větev 2 (výtok 550) | **2 250 l/h** | kbelík 5. 9. 2026, vír zavřený |

**0,4 bar u Green Resetu je maximální tlak nádoby, ne ztráta na pěnách.** Dřívější odvození „čistý filtr bere 4 m, a proto teče 950 l/h“ neplatí — čerpadlo s výtlakem 3,2 m by při 4 m ztráty nedalo vůbec nic.

---

## Rychlosti a dynamická výška

`v = Q / A`, `A₃₈ = 1,134·10⁻³ m²`, `A₅₀ = 1,963·10⁻³ m²`.

| Průtok | v v 38 mm | v²/2g v 38 mm | v v 50 mm | v²/2g v 50 mm |
| ---: | ---: | ---: | ---: | ---: |
| 950 l/h | 0,23 m/s | 0,3 cm | 0,13 m/s | 0,1 cm |
| 2 250 l/h | 0,55 m/s | **1,6 cm** | 0,32 m/s | 0,5 cm |
| 4 500 l/h | 1,10 m/s | **6,2 cm** | 0,64 m/s | 2,1 cm |

Dvě věci, které z toho plynou:

1. **Ztráta roste s druhou mocninou průtoku.** Co při 2 250 l/h nic nedělá, při 4 500 l/h bere čtyřnásobek. Původní cíl „4 000–5 500 l/h“ ve stávající 38mm trase proto není jen otázka čerpadla.
2. **Průměr rozhoduje s pátou mocninou** (`ztráta ∝ Q²/d⁵`). 50 mm má při stejném průtoku zhruba **čtvrtinovou** ztrátu proti 38 mm.

### Ztráty na metr a na tvarovku

| Prvek | Při 950 l/h | Při 2 250 l/h | Při 4 500 l/h |
| --- | ---: | ---: | ---: |
| Hladká hadice 38 mm, 1 bm | ~0,2 cm | ~1 cm | ~4 cm |
| **Spirálová (vroubkovaná) 38 mm, 1 bm** | ~0,5 cm | **~2–4 cm** | ~8–16 cm |
| Koleno 90° (K ≈ 0,5–1) | ~0,2 cm | ~1–1,6 cm | ~3–6 cm |
| Hladká 50 mm, 1 bm | ~0,05 cm | ~0,3 cm | ~1 cm |

**Kolena nejsou problém.** Deset kolen při 2 250 l/h je řádově 10–15 cm sloupce. Dřívější „sifonové oblouky přidávají kolena“ je pravda, ale v číslech to nic neváží. Váží **délka vroubkované hadice**, **průměr** a **výška**.

---

## Kde je čerpadlo na své křivce

Oase pro tyhle 12V modely nezveřejňuje celou křivku, jen dva krajní body (max. průtok při 0 m, max. výtlak při 0 l/h). Reálná křivka leží mezi lineární a kvadratickou spojnicí — proto všude **pásmo**, ne jedno číslo.

| Větev | Naměřeno | % katalogu | Odpor systému (lineární) | Odpor systému (kvadratická) |
| --- | ---: | ---: | ---: | ---: |
| 1 (6000) | 950 l/h | 16 % | 2,7 m | 3,1 m |
| 2 (12000) | 2 250 l/h | 20 % | 2,6 m | 3,1 m |

**Obě čerpadla běží skoro na doraz výtlaku.** Ze 3,2 m jim zbývá pár desítek centimetrů. To není „12 V je slabé“ — je to systém, který bere 2,6–3,1 m. Najít kde, ne kupovat další techniku.

---

## Větev 1 — je to skoro čistě výška

Při 950 l/h je rychlost v 38 mm **0,23 m/s**. Tření v hadici je pak řádově **0,5 cm/m** i u vroubkované; dvacet metrů dá 10–18 cm. Proti 2,7–3,1 m je to šum.

| Položka | Odhad při 950 l/h |
| --- | ---: |
| Hadice + kolena | 0,1–0,2 m |
| Green Reset, čisté pěny | 0,2–0,5 m |
| **Zbytek = statická výška** | **2,0–2,8 m** |

Rozpočet vychází jen tehdy, když je **hladina v IBC zhruba 2 až 2,8 m nad hladinou jezírka**. Číslo „~1,2 m“ jinde v dokumentaci s naměřenými 950 l/h nesedí.

### Test (pásmo, 10 minut)

Změřit **hladinu vody v IBC minus hladina jezírka**. Ne ode dna jámy, ne k hornímu okraji IBC — u ponorného čerpadla se počítá od hladiny k hladině.

- Vyjde **~2,5 m** → záhada je vyřešená a spodní tabulka platí.
- Vyjde **~1,2 m** → výšku to nevysvětluje a viník je jinde: ucpané pěny, dlouhá nebo zalomená hadice, propad napětí na 12 V kabelu, opotřebené oběžné kolo.

### Co udělá snížení IBC

Předpoklad: Green Reset + hadice berou 0,4 m, ty zůstávají.

| Hladina IBC nad jezírkem | Celkový odpor | Průtok (lineární) | Průtok (kvadratická) |
| ---: | ---: | ---: | ---: |
| **2,5 m (dnešní odhad)** | 2,9 m | 560 l/h | 1 840 l/h |
| 2,0 m | 2,4 m | 1 500 l/h | 3 000 l/h |
| 1,5 m | 1,9 m | 2 440 l/h | 3 820 l/h |
| 1,2 m | 1,6 m | 3 000 l/h | 4 240 l/h |

Naměřených 950 l/h leží přesně v pásmu pro 2,5 m. **Snížení IBC na 1,2–1,5 m je největší jednotlivý zisk v celém systému** — i pesimistický odhad je 2,5× víc vody, a to bez nákupu.

Dolní mez je daná gravitací: výtok IBC musí zůstat nad hladinou jezírka. Prakticky to znamená hladinu v IBC kolem **1,2–1,5 m**, ne níž. Přívod zaústit **pod hladinu v IBC**, ne volným pádem shora — čerpadlo pak zvedá k hladině, ne k hrdlu.

---

## Větev 2 — čísla nevycházejí

Při 2 250 l/h se dá poskládat jen část odporu:

| Položka | Odhad |
| --- | ---: |
| Netto statika při **funkčním** sifonu (výtok 550 nad jezírkem) | 0,1–0,3 m |
| Hadice 2× 40 / 38 mm, ~20 bm vroubkované | 0,2–0,8 m |
| T-kus, kolena, přechody | 0,1–0,2 m |
| 2× UV 55 W v sérii | 0,2–0,6 m |
| Biofiltr 550, čisté houby | 0,1–0,4 m |
| **Součet** | **0,7–2,3 m** |
| **Čerpadlo ale musí táhnout** | **2,6–3,1 m** |
| **Nevysvětlený zbytek** | **0,3–2,4 m** |

Čtyři kandidáti, každý s levným testem:

| Hypotéza | Test | Cena |
| --- | --- | ---: |
| **Ventil na větvi B je přiškrcený** (as-built ho popisuje jako „škrcená“) | Otevřít naplno, kbelík znovu | 0 Kč |
| **Sifon je přerušený vzduchem na hřebeni** — pak se počítá celá výška U, ne 0,2 m | Odvzdušnit vrchol za chodu; když ujde vzduch a průtok stoupne, je to ono | 0 Kč |
| Hadice je delší / zalomená / zanesená | Projít trasu, změřit bm | 0 Kč |
| Propad napětí na 12 V, opotřebené kolo | Změřit napětí na čerpadle za chodu | 0 Kč |

Dokud tohle nikdo neproměří, je každý nákup na větev 2 střelba naslepo.

### Vzduch na hřebeni — proč je to nejpravděpodobnější viník

Aby sifon fungoval, musí být celá trasa zaplavená. Vzduch ze sestupné větve se odnese, jen když voda teče dost rychle — orientačně **nad 0,6–1,0 m/s** v potrubí tohoto průměru.

Naměřená rychlost v 38 mm při 2 250 l/h je **0,55 m/s**. To je pod prahem. Bublina na hřebeni tedy **nemá jak sama odejít** a zůstane tam. A přesně tam je jediné místo, kde v tomto zapojení vzduch být může — v propoji mezi vrcholy obou lamp. (V samotných křemenkách ne, to platí dál: první lampa se plní zdola, druhá teče shora dolů.)

Když je hřeben zavzdušněný, čerpadlo netáhne 0,2 m netto statiky, ale **skutečnou výšku U — kolem 1,7 m**. To samo o sobě zavře skoro celý nevysvětlený zbytek v tabulce.

**Oprava:** automatický odvzdušňovací ventil nebo obyčejný kohout na nejvyšším bodě, cca **200–500 Kč**. Ne naklánět lampy.

Tím se také upřesňuje dřívější závěr z [lab.md](lab.md): „vrchol sifonu čerpadlo netíží“ platí **jen u zaplaveného sifonu**. Při 0,55 m/s to není samozřejmost, kterou lze předpokládat.

---

## Co s výtlakem udělá buben

Vana bubnu má **volnou hladinu**. Tím se sifon přeruší natrvalo a jeho výška se stane skutečnou statikou.

| Stav | Statika, kterou čerpadlo vidí |
| --- | --- |
| Dnes, sifon zaplavený | výtok 550 nad jezírkem, ~0,1–0,3 m |
| Dnes, sifon zavzdušněný | vrchol U, ~1,7 m |
| **S bubnem** | **hladina ve vaně bubnu, natrvalo** |

Kaskáda **UV → buben → 550 → jezírko** potřebuje tři schody nad hladinou jezírka, a vana bubnu je z nich nejvýš. Odhad **0,6–0,9 m** statiky natrvalo.

Kaskáda **UV → buben → jezírko** (bez 550 na této větvi) potřebuje schod jediný. Vana může sedět kolem **0,3–0,4 m** a ubere podstatně méně.

Bio tím netrpí: hlavní nitrifikace je 300 l Hel-X v IBC na větvi 1. 130 l hub v 550 je doplněk, který si v první variantě kupuje celý jeden schod výšky.

---

## Obsádka — kolik té zátěže vlastně je

Stav k **5. 9. 2026**: **5× Koi cca 40 cm** a **cca 20 mladých cca 8 cm** (výtěr před měsícem).

| Veličina | Odhad |
| --- | ---: |
| 5× 40 cm Koi | 5–6,5 kg |
| 20× 8 cm | ~0,2 kg |
| **Biomasa celkem** | **cca 5–7 kg** |
| Na 40 m³ | 0,15 kg/m³ |
| Na 20 m³ (viz níž) | 0,3 kg/m³ |
| Krmivo při 1 % biomasy | ~60 g/den |
| Produkce amoniaku (30 g TAN / kg krmiva) | **~1,8 g TAN/den** |
| Kapacita 118 m² Hel-X (0,3 g/m²/den) | ~35 g TAN/den |

**Rezerva biofiltru je řádově dvacetinásobná.** Běžná Koi jezírka jedou 0,5–1 kg/m³; tady je to zlomek.

Dva důsledky:

1. **Zákal není z ryb.** Pět kaprů nevyrobí zelenou vodu ve 20–40 m³. Živiny jdou ze slunce na celý 1,5m sloupec, z listí a prachu, z dopouštěné vody a z usazeniny na dně. Filtrace dimenzovaná na rybí kal řeší problém, který tady není.
2. **Buben ztrácí hlavní důvod.** Jeho největší přínos je odvést rybí kal dřív, než se rozloží. Při 5–7 kg biomasy není co odvádět.

Mladí ale porostou. Až bude 25 Koi kolem 40 cm, biomasa vyskočí zhruba **pětinásobně** a rozvaha o bubnu se otevře znovu.

---

## Objem — číslo, na kterém visí zbytek

Ovál ve 8 × 5 m má hladinu ~31 m². Na 40 m³ by průměrná hloubka musela být **1,27 m** při maximu 1,5 m, tedy skoro svislé stěny a plné dno. Rozvinutý profil takové vany je přes **90 m² fólie**.

Koupeno bylo **64,05 m²** (7 × 9,15 m, jeden kus). To sedí na miskovitý tvar se svahy kolem 45°, mělkou policí a úzkou hlubinou. Frustum se stejnými rozměry vychází na **cca 15–28 m³**.

Ověření je zadarmo: **vodoměr při dopouštění**, nebo pásmo a hloubkový profil po metru.

| Když je objem ~20 m³ místo 40 | Posun |
| --- | --- |
| Obrat obou větví za den | z 1,9× na **~3,8×** |
| UV na m³ | ze 4 W na **~8 W** |
| Dyofix dávkovaný na 40 m³ | zhruba **dvojnásobek** |
| Biomasa na m³ | 0,3 kg/m³ — pořád velmi málo |

---

## Optimalizace k průzračné vodě

Seřazeno podle poměru přínos / cena. První tři jsou zadarmo.

| # | Krok | Cena | Co přinese |
| ---: | --- | ---: | --- |
| 1 | **Změřit hladinu IBC nad jezírkem, pak IBC snížit** | 0 Kč + práce | Větev 1 z 950 na **2 400–4 200 l/h**. Největší zisk v systému. |
| 2 | **Otevřít ventil větve B naplno** | 0 Kč | As-built ho popisuje jako škrcený. Může být celý nevysvětlený zbytek. |
| 3 | **Odvzdušnit hřeben U za chodu** | 0 Kč | Zjistí, jestli sifon vůbec funguje. |
| 4 | **Kohout / automatický odvzdušňovák na vrcholu** | 200–500 Kč | Trvalé řešení bubliny, která při 0,55 m/s sama neodejde. |
| 5 | **UV paralelně, ne v sérii** | 600–1 200 Kč | Stejná dávka na litr, **cca 8× nižší odpor** dvojice. |
| 6 | **50 mm co nejdál k lampám** | 1 500–3 000 Kč | Čtvrtinová ztráta proti 38 mm. Na trnech lamp zůstane 38 mm. |
| 7 | **Osázet 30cm polici** | 3 000–8 000 Kč | Při 5 Koi rostliny přežijí. Odebírá živiny řasám u zdroje. |
| 8 | **Vazač fosfátu na výtoku IBC** | 1 000–2 000 Kč | Při téhle obsádce je limitace fosforem reálně dosažitelná. |
| 9 | **Přehodnotit Dyofix** | −  | Pravděpodobně dvojnásobná dávka. Stíní i rostliny z kroku 7. |
| 10 | **Buben odložit** | — | Málo rybího kalu, bere výtlak, na mrtvou řasu je to nejhorší typ síta. |

### Proč zrovna tohle pořadí

Kroky 1 až 6 dělají jednu věc: **víc vody přes stávající UV**. Wattů je dost (160 W), dávka na průchod je při dnešních průtocích dokonce zbytečně dlouhá. Chybí počet průchodů za den.

Kroky 7 až 9 řeší **živiny**, ne filtraci. Při 5–7 kg ryb ve 20–40 m³ je zelená voda otázka slunce a fosforu, ne rybího kalu. Osázená police a vazač fosfátu berou řasám vstup; UV a síto jen uklízejí následek.

### Buben — kdy ho vrátit do hry

- Až mladí Koi vyrostou a biomasa půjde přes ~25 kg.
- Nebo až kroky 1–6 zvednou průtok na větvi 2 tak, že je z čeho ubrat.

Až na to dojde: vanu **co nejníž**, variantu **UV → buben → jezírko** zvážit dřív než tři schody s 550, prací vodu na zahradu a **dopouštění počítat**. Ostřik chce kolem 2 bar a řídicí elektroniku — u koupací vody to je 230 V se stejnou vážností, s jakou repo odmítá 230 V čerpadla.

---

## Co v tomto souboru neplatí za pravdu

- **Křivky čerpadel.** Oase dává jen krajní body. Všechna pásma jsou interpolace mezi lineární a kvadratickou spojnicí.
- **Délka a typ hadic.** Nezměřeno. Ztráty na metr jsou tabulkové pro vroubkovanou hadici, ne pro tuhle trasu.
- **Ztráta v UV a v 550.** Odhad z třídy zařízení, ne z manometru.
- **Objem jezírka.** Dopočet z geometrie a fólie, ne z vodoměru.

Dva manometry (před UV a za UV) nebo prostě kbelík po každé jednotlivé změně tenhle soubor nahradí měřením.
