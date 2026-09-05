# Provoz a zapojení — krok za krokem

Čísla níže jdou v pořadí prací. 12V čerpadla, Green Reset i IBC se nemění. Satelit, druhý tlakový filtr a stálý zeolit/uhlí se neinstalují.

## 0. Nejdřív to, co je zadarmo

Rozpočet výtlaku v [hydraulika.md](hydraulika.md) říká, že obě čerpadla běží skoro na doraz (2,6–3,1 m ze 3,2 m) a **část toho odporu není vysvětlená**. Než se cokoliv kupuje nebo instaluje:

1. **Změřit hladinu v IBC nad hladinou jezírka** pásmem. Při 950 l/h je tření zanedbatelné — je to skoro čistě výška. Snížení IBC na 1,2–1,5 m znamená **2 400–4 200 l/h** místo 950.
2. **Otevřít ventil větve B naplno.** As-built ho popisuje jako škrcený.
3. **Odvzdušnit vrchol U u lamp za chodu.** Při 0,55 m/s bublina sama neodejde a zavzdušněný hřeben stojí čerpadlo ~1,7 m místo 0,2 m.
4. Po každé změně **kbelík**, jednu změnu po druhé.

Teprve pak má smysl mluvit o hadicích, paralelním UV a bubnu.

---

## 1. Diagnostika zákalu a kbelíkový test

Nejdřív vzhled vody, pak čísla. Média a ventily se ladí podle barvy, ne podle katalogu.

### Typ zákalu

| Vzhled | Co to je | Co zvedne průzračnost |
| --- | --- | --- |
| Zelená | Jednobuněčné řasy | Víc vody přes UV 2×55 W; živiny dolů (osázená police, vazač fosfátu) |
| Hnědá / prachová | Zvířený kal, detrit | Buben + 550; mírný vír **ne** do 30cm police; občas vysavač v 1,5 m |
| Mléčná | Bakterie, rozpuštěná organika | Méně krmení, kyslík v hlubině, odvoz kalu z bubnu na zahradu |
| Žlutá, ale čirá | Rozpuštěné organiky (DOC) | Výměna vody; uhlí jen 7–14 dní **bez** Dyofixu |

Celý objem je v dosahu slunce (max. 1,5 m). Zelená voda je u tohoto tvaru očekávatelná — proto UV a odběr živin, ne další houby v tlaku.

**Zákal není z ryb.** Obsádka k 5. 9. 2026 je **5× Koi cca 40 cm + cca 20 mladých cca 8 cm**, dohromady kolem **5–7 kg**. To je zlomek běžné Koi zátěže a biofiltr má proti tomu asi dvacetinásobnou rezervu. Živiny pro řasy jdou ze slunce, listí, dopouštěné vody a usazeniny na dně — ne z rybího kalu.

### Kbelíkový test

Měřit na **výtoku z Biofiltru 550** (větev 2) a zvlášť na **výtoku z IBC** (větev 1). Ne u čerpadla.

1. Kbelík 10 l, stopky.
2. Plný kbelík: `průtok (l/h) = 10 / sekundy × 3600`.
3. **Po každé jednotlivé změně znovu.** Dvě změny naráz = nikdo neví, co zabralo.
4. Výchozí hodnoty **5. 9. 2026**: větev 1 **950 l/h**, větev 2 **2 250 l/h** ([lab.md](lab.md)).
5. Cíl není katalogové číslo. Cíl je **odebrat systému odpor** — obě čerpadla dnes táhnou 2,6–3,1 m ze 3,2 m ([hydraulika.md](hydraulika.md)).

---

## 2. Větev 2 — víc vody přes stávající lampy

Buben je **odložený** (viz níž). Cílem téhle větve je počet průchodů přes 110 W, ne další stupeň v řadě.

```
Aquamax 12000 12V
  --50 mm--> T-kus
               |-- větev A: vír podél oválu --> jezírko
               |-- větev B: UV 2×55 W paralelně --> Invital 550 --> jezírko
                              odvzdušnění na nejvyšším bodě
```

### Hadice

- Od čerpadla k T-kusu **jedna 50 mm**. Neslučovat dvě 40 mm Y jako „vstup 50 mm“ — víc ztrát, nerovnoměrné dělení.
- 50 mm vést **co nejdál k lampám**; na trnech lamp zůstane **38 mm** (strop analogu Vitronic).
- Ztráta jde s `Q²/d⁵`: 50 mm má při stejném průtoku zhruba **čtvrtinovou** ztrátu proti 38 mm.
- Dvě 40 mm až **za** 550 jako dvě mírné vratné trysky, ne jako vstup do filtru.

### UV paralelně, ne v sérii

Každá lampa dostane **půlku průtoku**, takže v ní voda stráví dvakrát déle. Dávka na litr proto vyjde **stejně jako v sérii**, ale odpor dvojice spadne zhruba **osmkrát** (`k·Q²/4` místo `2·k·Q²`).

Dřívější tvrzení „paralelně by rozdělilo dávku na průchod“ v tomto souboru **neplatilo** a bylo důvodem, proč se paralelní zapojení zamítalo.

- Materiál: 2 T-kusy a ~2 m hadice 38 mm.
- Hadice k oběma lampám **stejně dlouhé**, jinak se tok rozdělí nerovnoměrně.
- Až průtok vzroste, dávka na průchod klesne úměrně. To je záměr: kontakt je dnes zbytečně dlouhý, chybí počet průchodů.
- Když jedna lampa zhasne, polovina vody projde bez dávky. Kontrolovat obě.

### Odvzdušnění hřebene

Na nejvyšší bod trasy patří **kohout nebo automatický odvzdušňovák** (200–500 Kč). Při 0,55 m/s se bublina z hřebene sama neodnese a zavzdušněný sifon stojí čerpadlo ~1,7 m místo ~0,2 m. Detail v [hydraulika.md](hydraulika.md).

### Výšky

Výtok 550 musí zůstat **nad** hladinou jezírka, jinak nepoteče gravitací. Za UV je vše netlakové.

Každý schod nad hladinou jezírka je **trvalá statika**, jakmile na něm je volná hladina. Dokud je trasa zaplavená až do jezírka, sifon výšku vrací zpátky — proto na hřeben odvzdušňovák a proto se nepřidávají otevřené vany bez důvodu.

### Biofiltr 550

Houby dělají dočištění. Jemná japonská rohož na výstupu je volitelná a je to zatím **levnější odpověď na shluky z UV než buben**: řasa zabitá UV má pod 2 µm a chytá se jen jako vločka. Čistit, až stoupne hladina ve 550, ne obě komory naráz.

### Křemenky UV

**Křemenka** je křemenná trubice kolem UV-C zářivky: zářivka v ní nesmí do vody, voda teče okolo a UV-C prochází sklem. Obyčejné sklo by záření sežralo. Náhradní díl v e-shopu je „křemenná trubice“ / quartz sleeve — to není zářivka.

Předfiltrace před lampami je jen sání u hladiny, takže se pouzdra špiní. Otírat, jinak 110 W svítí do mlhy.

### Orientace UV — svislé U

As-built: 1. lampa **zdola nahoru**, propoj **nahoře**, 2. lampa **shora dolů**, police **~1 m** (havárie mimo elektro). **Nesnižovat na hladinu.** Komory jsou plné — bublina v křemence u tohoto U není a náklon na tom nic nezmění. Po přepojení na paralelní zapojení zůstávají obě lampy nastojato na téže polici, jen dostanou vlastní přívod.

Vzduch se v téhle trase drží **na hřebeni propoje**, ne v pouzdrech, a při 0,55 m/s sám neodejde — proto odvzdušňovák, ne přeložení lamp.

Sifon zpět pod hladinu po stopu čerpadla může vysát ovál — výtok 550 nad hladinou nebo přisátí vzduchu na hřebeni.

### Třetí 55 W UV — nekupovat

Wattů je dost: **2×55 W + 2×25 W = 160 W**. I na 40 m³ to je 4 W/m³ (běžně stačí 2–4); při reálném objemu kolem 20 m³ dokonce ~8 W/m³. Úzké hrdlo je **počet průchodů**, ne watty.

Další 55 W: ~1,3 kWh/den, další křemenka, větší ztráta výtlaku. Nejdřív kroky z kapitoly 0 a paralelní zapojení.

---

## 3. Vír

Proud vody v oválu je **vír**. Výr je sova.

Kbelík 5. 9. 2026 při **zavřeném víru**: jen **2 250 l/h** přes UV — přebytek na obchoz není a A by lampám ještě ubrala.

- Teď: A **zavřená**. Otevřít až po krocích z kapitoly 0 a novém kbelíku.
- Trysku vést **podél hlubšího oválu**, ať vodu z 30cm police stahuje ke skimmeru / k sání 12000.
- **Nesměřovat** trysku do 30 cm mělčiny (zvíří dno, mléčná voda, bije do nohou, a jsou tam letošní mladí).

Mělká zóna 30 cm (šířka 0,3–1,5 m) je past na kal a vláknité řasy. Pohyb ano, tornado ne.

**Zavřený vír má cenu, ale i daň:** ovál pak skoro necirkuluje a kal se usadí tam, kde na něj filtrace nedosáhne. Sání 12000 je u hladiny a satelit byl zamítnut, takže dno řeší **vysavač**, ne žádný stupeň v řadě. Až kroky z kapitoly 0 zvednou průtok, mírný vír podél oválu je součást odpovědi na průzračnost, ne konkurent UV.

---

## 4. Větší tlakový filtr na větev 2 — neinstalovat

Úzké hrdlo je výtlak 12V (max. **3,2 m**), ne průměr hadice.

Největší běžný hobby tlak s 50 mm (řádově Oase FiltoClear 31000): max. **0,2 bar (= 2 m)**, set s AquaMax 17000 230 V. Sériově s UV a 550 by 12V čerpadlo udusil — a to už teď táhne 2,6–3,1 m ze 3,2 m.

Green Reset na větvi 1 už tlakové houby + UV dělá.

**[SUNSUN CPF-10000](https://www.jezirkabanat.cz/tlakovy-filtr-sunsun-cpf-10000-x14955)** (3 749 Kč, kód B04842) před 2×55 W na větvi 2 **nedávat**, ani se silnějším čerpadlem.

| | CPF-10000 | Větev 2 / jezírko |
| --- | --- | --- |
| Nádoba | 25 l, 5 pěnovek | Green Reset už 100 l |
| Max. tlak | **0,3 bar ≈ 3 m** | Aquamax 12000 12 V má strop 3,2 m |
| Hadice | max. **38 mm** | 50 mm k T-kusu |
| Vestavěné UV | **11 W** | už **2×55 W** (+ 2×25 W v Green Resetu) |

Silnější čerpadlo tlakové hobby víko nespásí — strop zůstane ~3 m vodního sloupce; 230 V by navíc zrušilo 12 V u koupání. Pěny **před** UV křemenky trochu šetří, ale zelený zákal nechytí.

Bead / bazénový písek chtějí 0,8–1,5 bar — 12V to neutáhne.

Kdyby tlak přesto: jen ≤0,2 bar, 50 mm v kuse, **místo** bubnu v řadě. Pro průzračnost krok zpět.

---

## 5. Satelitní dnové sání — neinstalovat

Vyzkoušeno: malý dopad, v zimě vadí Koi, v 1,5 m koupání překáží lidem. Náhrada dna v tomto systému není. Kal v nejhlubším místě nechat v klidu, občas vysavač.

Důsledek, který je potřeba vyslovit: **sání obou větví je u hladiny**. Co se usadí na dně, žádný stupeň v řadě nevidí — ani buben. Dno je práce pro vysavač.

---

## 6. Zeolit, uhlí, písek — ne jako stálá náplň na průzračnost

Průhlednost v tomto oválu zvedne **víc průchodů přes stávající UV** a **méně živin pro řasy** (kapitola 0 a 6b). Zeolit bere **NH₄**, uhlí **žlutý DOC a Dyofix**. Řasy ani kalový prach nesberou.

| Médium | Rozhodnutí | Proč |
| --- | --- | --- |
| Zeolit | Nekupovat kvůli zákalu | Nouzový sáček 5–10 kg jen při špičce amoniaku, pak ven. Nasycený NH₄ pouští zpět. |
| Aktivní uhlí | Ne se Dyofixem | Vytáhne barvivo i žlutý DOC. Max. 7–14 dní, jen bez barviva, pak vyjmout. |
| Bazénový písek | Ne na 12V | Chce 0,8–1,5 bar. |

Zeolit je při 5–7 kg biomasy skoro jistě zbytečný: biofiltr má proti téhle zátěži asi dvacetinásobnou rezervu.

### Kam (jen krátká kúra)

Ani jedno **ne** do Green Resetu (dusí 12 V výtlak), **ne** do vířícího Hel-X (oděr, lůžko je biofilm).

| Médium | Místo |
| --- | --- |
| Zeolit | Síťka v **IBC až za Hel-X**, u klidného výtoku |
| Uhlí | Síťka na **výtoku IBC**, nebo **poslední komora 550** |

### Pořadí, když jdou obě kúry

Od ryb, ne od vzhledu. Souběžně v pytlích to nemá smysl.

1. Změřit **NH₄ / NO₂**. Při amoniaku nejdřív zeolit.
2. Až je NH₄ v nule, zeolit **ven**.
3. Uhlí až potom: voda **žlutá a jinak čirá**, **bez Dyofixu**. Dokud Pond Blue v jezírku je, uhlí nedávat.

---

## 6b. Živiny — hlavní páka na zelenou vodu

Při **5–7 kg ryb** v 20–40 m³ nevzniká zelená voda z rybího kalu. Vzniká ze slunce na celý 1,5m sloupec a z živin, které do jezírka lezou jinudy: listí, prach, pyl, dopouštěná voda, usazenina na dně. Filtrace uklízí následek. Tohle bere řasám vstup.

### Osázet 30cm polici

Původní návrh polici odepsal jako past na kal, protože počítal se 40 Koi. **Pět kaprů rostliny nezničí.** Police 30 cm, široká 0,3–1,5 m, je přesně regenerační zóna, kterou koupací jezírka běžně mají.

- Rostliny berou dusík a fosfor přímo z vody, celou sezónu, bez elektřiny.
- Stíní dno mělčiny, takže tam nestartují vláknité řasy.
- Mladí Koi v nich mají úkryt.
- Substrát chudý (praný štěrk), ne zahradní zemina — ta by živiny naopak dodala.
- Tryska víru sem pořád **nesmí**.

### Vazač fosfátu

Fosfor je u takhle lehké obsádky reálně limitovatelný. Vazač (na bázi železa nebo lanthanu) v síťce na **výtoku IBC**, u klidného proudu.

- Nejdřív **změřit PO₄**. Bez čísla se dávkovat nedá.
- Vazač je vyčerpatelný, po sezóně ven a nový.
- Do vířícího Hel-X ne (oděr), do Green Resetu ne (tlak).

### Dyofix přehodnotit

Dávka byla počítána na 40 m³. Při reálném objemu kolem 20 m³ je to zhruba **dvojnásobek**. Barvivo navíc stíní i rostliny z kapitoly výš, takže si kroky protiřečí.

Pořadí: nejdřív osázet polici a nechat ji chytit, pak nechat Dyofix vyblednout a **nedávkovat znovu**. Kdyby se voda bez barviva zezelenala, vrátit se ke slabší dávce.

### Krmení

Pět kaprů a dvacet mladých sní velmi málo. Každé zbylé zrno je fosfor pro řasy. Krmit tak, aby bylo do dvou minut po krmivu; mladým spíš častěji a po troškách než jednou hodně.

---

## 6c. Buben — odložit

Buben je koupený, ale jako **další** krok je předčasný.

| Co se čekalo | Jak to je při 5–7 kg biomasy |
| --- | --- |
| Odvede rybí kal dřív, než se rozloží | Hlavní přínos bubnu — jenže tolik kalu tu nevzniká |
| Zachytí řasu zabitou UV | Buňky mají pod 2 µm, síta bývají 60–120 µm. Chytí jen vločky a při odumření se rychle zaslepí |
| Neovlivní průtok | **Ovlivní.** Volná hladina ve vaně přeruší sifon natrvalo, viz [hydraulika.md](hydraulika.md) |
| Sebere kal ze dna | Ne. Sání je u hladiny |
| Zapadne do 12V konceptu | Ostřik chce ~2 bar a řídicí elektroniku — 230 V u koupací vody |

**Kdy ho vrátit do hry:** až letošní mladí vyrostou a biomasa půjde přes ~25 kg, nebo až kroky z kapitoly 0 zvednou průtok tak, že je z čeho ubrat.

Až na to dojde: vanu **co nejníž**, zvážit **UV → buben → jezírko** místo tří schodů s 550, přepad mimo sání 12000, prací vodu na zahradu a započítat dopouštění. Zima: ostřik a elektronika nesmí zmrznout — bypass nebo nezámrzná šachta.

Levnější mezikrok na shluky z UV: **jemná japonská rohož** v poslední komoře 550.

---

## 7. Dva měřiče (teplota, pH, EC)

Zákal neměří; oddělí řasy od chemie.

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

Green Reset (tlak), vířící Hel-X (oděr, bubliny), UV (UV-C ničí elektrody).

pH elektroda nesmí vyschnout; kalibrace ze začátku po 2 týdnech, pak měsíčně; v mrazu sundat. EC je venku stabilnější.

### Kapky, které dva přístroje nenahradí

Jednou pořádně změřit a mít základní linii. Při 5–7 kg biomasy to není akutní, ale je to laciné a bez toho se dávkuje naslepo.

| Test | Proč zrovna teď |
| --- | --- |
| **KH** | Nejdůležitější. Nitrifikace ji spotřebovává a zelená voda dělá velké denní výkyvy pH. Nízké KH = houpačka pH. |
| **PO₄** | Vstup pro vazač fosfátu z kapitoly 6b. Bez čísla se dávkovat nedá. |
| NH₄ / NO₂ | Kontrola, ne poplach. Letošní mladí jsou na dusitany citlivější než dospělí. |
| NO₃ | Trend přes sezónu, ukazatel zátěže živinami. |

| Čtení | Vzhled vody | Význam |
| --- | --- | --- |
| pH/EC v normě | Zelená | Řasy, ne chemie → víc průchodů přes UV, míň živin |
| Rostoucí EC | Mléčná / hnědá | Zátěž, málo odkalu / výměny — zeolit zákal nesebere |
| Ranní pH pod ~6,8 | Mléčná | Organika a CO₂ → vzduch v hlubině, méně krmení |
| EC v normě | Žlutá, čirá | DOC → výměna vody nebo krátké uhlí bez Dyofixu |

Orientačně: pH 7,0–8,2, EC stovky µS/cm podle zdroje vody. Důležitější je stabilita než ideální číslo.

---

## Větev 1 — snížit IBC

Tady je největší jednotlivý zisk v celém systému a nic se pro něj nekupuje.

- **Změřit hladinu v IBC nad hladinou jezírka** pásmem. Ne ode dna jámy, ne k hornímu okraji nádrže.
- Při 950 l/h je tření v hadici zanedbatelné, takže těch 2,7–3,1 m odporu je skoro celé výška. Snížení na 1,2–1,5 m znamená **2 400–4 200 l/h** ([hydraulika.md](hydraulika.md)).
- Dolní mez je gravitace: výtok IBC musí zůstat nad hladinou jezírka.
- Přívod zaústit **pod hladinu v IBC**, ne volným pádem shora.
- Green Reset čistit podle **výtoku z IBC**, odpad z režimu čištění na zahradu, ne do IBC.
- Skimmer je jen **koš**; hladinu táhne Aquamax 6000. Druhé čerpadlo do stejného Green Resetu **ne**. Při 950 l/h stěnový skimmer hladinu prakticky netáhne — po zvýšení průtoku se to zlepší samo.
- Hel-X neměnit, dokud médium víří a teče voda.

V horku: vzduchovací kámen v hlubině mimo brouzdaliště. Nebrat vzduch Hel-X tak, aby přestaly rotovat.

---

## Co cíleně nedělat

- Větší tlakový filtr na větev 2, včetně SUNSUN CPF-10000 před UV.
- Vstup 2×40 mm Y místo 50 mm.
- Bead / bazénový písek na 12V.
- Tryska do 30cm zóny.
- Satelit na dno.
- Stálý zeolit na zákal, uhlí + Dyofix.
- Druhé čerpadlo za Green Reset.
- Silnější čerpadlo kvůli hobby tlaku (strop ~0,3 bar).
- Další 55 W UV — wattů je dost (50 + 110 W).
- **Instalovat buben, dokud neproběhnou kroky z kapitoly 0.**
- **Naklánět lampy kvůli průtoku.** Vzduch je na hřebeni, ne v křemenkách; patří tam odvzdušňovák.
