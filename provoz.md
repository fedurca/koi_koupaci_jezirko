# Provoz a zapojení — krok za krokem

Čísla níže jdou v pořadí prací. 12V čerpadla, Green Reset i IBC se nemění. Satelit, druhý tlakový filtr a stálý zeolit/uhlí se neinstalují.

---

## 1. Diagnostika zákalu a kbelíkový test

Nejdřív vzhled vody, pak čísla. Média a ventily se ladí podle barvy, ne podle katalogu.

### Typ zákalu

| Vzhled | Co to je | Co zvedne průzračnost |
| --- | --- | --- |
| Zelená | Jednobuněčné řasy | Víc vody přes UV 2×55 W + buben za nimi; volitelně Dyofix |
| Hnědá / prachová | Zvířený kal, detrit | Buben + 550; mírný výr **ne** do 30cm police; občas vysavač v 1,5 m |
| Mléčná | Bakterie, rozpuštěná organika | Méně krmení, kyslík v hlubině, odvoz kalu z bubnu na zahradu |
| Žlutá, ale čirá | Rozpuštěné organiky (DOC) | Výměna vody; uhlí jen 7–14 dní **bez** Dyofixu |

Celý objem je v dosahu slunce (max. 1,5 m). Zelená voda je u tohoto tvaru očekávatelná — proto UV a buben, ne další houby v tlaku.

### Kbelíkový test

Měřit na **výtoku z Biofiltru 550** (větev 2) a zvlášť na **výtoku z IBC** (větev 1). Ne u čerpadla.

1. Kbelík 10 l, stopky.
2. Plný kbelík: `průtok (l/h) = 10 / sekundy × 3600`.
3. Cíl větve 2 po zapojení bubnu: **4000–5500 l/h**.
4. Strop bubnu je **6000 l/h**. Nad ním teče voda přepadem **neošetřená** zpět do jezírka.
5. IBC: zapsat výchozí hodnotu (u 6000 12V a zdvihu +1,2 m často 1500–3000 l/h čistý Green Reset). Nesnažit se honit větev 1 na 6000 — čerpadlo na to nemá výtlak.

Když buben pere nonstop, stáhnout větev B (víc na výr), nepřidávat průtok.

---

## 2. Zapojení bubnu (větev 2)

Pořadí je dané kvůli průzračnosti: UV shlukne řasy, síto je zachytí, 550 jen leští.

```
Aquamax 12000 12V
  --50 mm--> T-kus
               |-- větev A: výr podél oválu --> jezírko
               |-- větev B: UV 2×55 W --> buben --> Invital 550 --> jezírko
                              buben přepad --> jezírko (mimo sání 12000)
                              buben prací odpad --> zahrada
```

### Hadice

- Od čerpadla k T-kusu **jedna 50 mm**. Neslučovat dvě 40 mm Y jako „vstup 50 mm“ — víc ztrát, nerovnoměrné dělení.
- Větev B smí jít 40 mm do UV, pokud UV větší trn nemá.
- Dvě 40 mm až **za** 550 jako dvě mírné vratné trysky, ne jako vstup do filtru.

### Výšky (za UV je vše netlakové)

1. Výtok z UV **nad** provozní hladinu bubnu.
2. Čistý výtok bubnu **nad** vtok Invital 550.
3. Výtok 550 **nad** hladinu jezírka.
4. Havarijní přepad bubnu: volný spád do jezírka, vyústění **mimo** sání 12000.

Bez tohoto schodu 550 nepoteče a buben poleje okolí.

### Přepad vs. praní

- Přepad = nouze, voda zpět do jezírka (neošetřená).
- Prací/odkalovací voda ze síta = koncentrovaná špina na **zahradu**, ne do 550, ne do IBC, ideálně ne zpět do jezírka.

### Biofiltr 550

Po bubnu nechat stávající houby jako dočištění. Jemná japonská rohož na výstupu je volitelná. Čistit, až stoupne hladina ve 550, ne obě komory naráz.

### Zima

Ostřik a elektronika bubnu nesmí zmrznout: bypass (UV → 550 nebo UV → jezírko) nebo nezámrzná šachta.

### Křemenky UV

Při pořadí UV → buben se pouzdra špiní rychleji (předfiltrace je jen sání u hladiny). Otírat, jinak 110 W svítí do mlhy. Kdyby UV přestalo být vidět, teprve pak zvážit buben **před** UV — pro zelenou vodu je to horší (shluky skončí v 550).

---

## 3. Whirlpool / výr

Neškrtit větev A natvrdo. Je to **obchoz** přebytku Aquamax 12000 nad stropem bubnu.

- Ventil B nastavit kbelíkem na 4000–5500 l/h na výtoku 550.
- Větev A nechat otevřenou tak, aby na bubnu zůstal limit, ne aby všecko šlo na síto.
- Trysku vést **podél hlubšího oválu**, ať vodu z 30cm police stahuje ke skimmeru / k sání 12000.
- **Nesměřovat** trysku do 30 cm mělčiny (zvíří dno, mléčná voda, bije do nohou).

Mělká zóna 30 cm (šířka 0,3–1,5 m) je past na kal a vláknité řasy. Pohyb ano, tornado ne.

---

## 4. Větší tlakový filtr na větev 2 — neinstalovat

Úzké hrdlo je výtlak 12V (max. **3,2 m**), ne průměr hadice.

Největší běžný hobby tlak s 50 mm (řádově Oase FiltoClear 31000): max. **0,2 bar (= 2 m)**, katalog **7,5 m³ s Koi**, set s AquaMax 17000 230 V. Na 40 m³ / 40 Koi to není skok v čistotě; sériově s UV + bubnem + 550 12V čerpadlo udusí.

Green Reset na větvi 1 už tlakové houby + UV dělá. Buben má jemnější záchyt než houby a pere se sám.

Bead / bazénový písek chtějí 0,8–1,5 bar — 12V to neutáhne.

Kdyby tlak přesto: jen ≤0,2 bar, 50 mm v kuse, **místo** bubnu v řadě. Pro průzračnost krok zpět.

---

## 5. Satelitní dnové sání — neinstalovat

Vyzkoušeno: malý dopad, v zimě vadí Koi, v 1,5 m koupání překáží lidem. Náhrada dna v tomto systému není. Kal v nejhlubším místě nechat v klidu, občas vysavač. Buben čistí to, co obíhá ve sloupci.

---

## 6. Zeolit, uhlí, písek — ne jako stálá náplň na průzračnost

| Médium | Rozhodnutí | Proč |
| --- | --- | --- |
| Zeolit | Nekupovat kvůli zákalu | Bere NH₄, ne řasy ani prach; při 40 Koi se rychle nasytí. Nanejvýš nouzový sáček 5–10 kg v IBC při špičce amoniaku, pak ven. |
| Aktivní uhlí | Ne se Dyofixem | Vytáhne barvivo i žlutý DOC. Max. 7–14 dní na výtoku IBC nebo v 550, jen bez barviva, pak vyjmout. |
| Bazénový písek | Ne na 12V | Chce 0,8–1,5 bar. Za bubnem je to duplicita sita. |

Dyofix u 1,5 m hloubky stíní dno (víc smyslu než v hlubokém jezírku). S bubnem + UV lze později zkusit slabší dávku. Uhlí nepořizovat, dokud barvivo zůstane.

---

## 7. Dva měřiče (teplota, pH, EC)

Zákal neměří; oddělí řasy od chemie a hlídají 40 Koi.

### Měřič 1 — jezírko

- Děrovaná KG/PVC šachta v **hlubině**, sonda v **~0,7–1 m**.
- Ne na 30cm polici (přehřev, slunce, lidé).
- Mimo vratné trysky, skimmer a dosah Koi.
- Ranní pH (noční CO₂), teplota pro krmení, trend EC (odpar, krmení, skok = něco se rozpustilo).

### Měřič 2 — výtok IBC

- Žlábek / nádobka **za** Hel-X, **před** smícháním s jezírkem.
- pH tu bývá o 0,1–0,4 nižší (nitrifikace). Rozestup vs. jezírko se zvětšuje = bio jede / klesá KH.
- Teplota IBC (vzduchování chladí). EC má kopírovat jezírko.

### Kam sondy nedávat

Green Reset (tlak), vířící Hel-X (oděr, bubliny), UV (UV-C ničí elektrody), vana bubnu (kolísání, ostřik).

pH elektroda nesmí vyschnout; kalibrace ze začátku po 2 týdnech, pak měsíčně; v mrazu sundat. EC je venku stabilnější. Občas kapky NH₄ / NO₂ / NO₃ / PO₄ — tohle dva přístroje nenahradí.

| Čtení | Vzhled vody | Význam |
| --- | --- | --- |
| pH/EC v normě | Zelená | Řasy, ne chemie → UV, buben, křemenky, případně Dyofix |
| Rostoucí EC | Mléčná / hnědá | Zátěž, málo odkalu / výměny — zeolit zákal nesebere |
| Ranní pH pod ~6,8 | Mléčná | Organika a CO₂ → vzduch v hlubině, méně krmení |
| EC v normě | Žlutá, čirá | DOC → výměna vody nebo krátké uhlí bez Dyofixu |

Orientačně: pH 7,0–8,2, EC stovky µS/cm podle zdroje vody. Důležitější je stabilita než ideální číslo.

---

## Větev 1 (jen provoz, bez přestavby)

- Green Reset čistit podle **výtoku z IBC**, odpad z režimu čištění na zahradu, ne do IBC.
- Vestavěné 230 V čerpadlo skimmeru **ne** do stejného Green Resetu souběžně s Aquamax 6000.
- IBC / Hel-X neměnit, dokud médium víří a teče voda. Snížení IBC a přepážka nejsou v tomto kroku.

V horku: vzduchovací kámen v hlubině mimo brouzdaliště (40 Koi, 1,5 m, málo nočního kyslíku). Nebrat vzduch Hel-X tak, aby přestaly rotovat.

---

## Co cíleně nedělat

- Větší tlakový filtr na větev 2 (sériově s bubnem nebo jako náhrada sita).
- Vstup 2×40 mm Y místo 50 mm.
- Bead / bazénový písek na 12V.
- Tryska do 30cm zóny.
- Satelit na dno.
- Stálý zeolit na zákal, uhlí + Dyofix.
- Druhé čerpadlo za Green Reset.
- Další UV — wattů je dost (50 + 110 W), chybělo síto za nimi a průtok skrz ně.
