# Changelog

Formát podle [Keep a Changelog](https://keepachangelog.com/cs/1.1.0/), verze podle [Semantic Versioning](https://semver.org/lang/cs/).

## [Unreleased]

## [1.2.0] — 2026-09-05

### Added

- [hydraulika.md](hydraulika.md) — rozpočet výtlaku obou větví, rychlosti, ztráty na metr a na tvarovku, testy na nevysvětlený odpor, seznam optimalizací k průzračné vodě.
- [doporuceni.md](doporuceni.md) — revize celého návrhu: 13 nálezů, obrat objemu, sifon, UV sériově vs. paralelně, co buben opravdu udělá, pořadí kroků.
- [provoz.md](provoz.md) — kapitola 0 (kroky zadarmo), 6b živiny (osázet 30cm polici, vazač fosfátu, Dyofix, krmení), 6c buben odložit.

### Changed

- **Obsádka: 5× Koi cca 40 cm + cca 20 mladých cca 8 cm** (výtěr srpen 2026), biomasa 5–7 kg — ne 40 Koi. Biofiltr má proti tomu asi dvacetinásobnou rezervu, takže zelená voda není z rybího kalu.
- **Buben odložen.** Vana s volnou hladinou přeruší sifon a sníží průtok větve 2; při téhle biomase navíc není co odvádět.
- **UV paralelně, ne v sérii** — při stejném průtoku stejná dávka a zhruba osminový odpor dvojice.
- **950 l/h na větvi 1 není strop.** Je to skoro čistá statika k IBC; po snížení nádrže na 1,2–1,5 m vychází 2 400–4 200 l/h.
- Objem jezírka označen za neověřený: 64 m² fólie nesedí na 40 m³, geometrie dává 15–28 m³.
- Na nejvyšší bod trasy patří **odvzdušňovák** — při 0,55 m/s bublina z hřebene sama neodejde.

### Fixed

- „Paralelně by rozdělilo dávku na průchod“ — chybné odvození, kterým se paralelní zapojení UV zamítalo.
- „Green Reset až 0,4 bar = 4 m, udusí čerpadlo i prázdný“ — 0,4 bar je max. tlak nádoby, ne ztráta na pěnách.
- Rozpor 40 mm vs. 38 mm na trnech UV; Green Reset 100 doplněn o katalogových ~9 m³ s Koi.

## [1.1.5] — 2026-09-05

### Changed

- UV U: **nesnižovat na hladinu**; 45° není půlka účinku (plné komory ⇒ dávka stejná). Náklon **+0–5 %** l/h. 38 mm na trnech lamp, 50 mm jen k T-kusu.

## [1.1.4] — 2026-09-05

### Changed

- UV: dvě lampy jako **svislé U** (zdola nahoru, propoj nahoře, shora dolů) — komory plné; náklon průtok skoro nezvedne. 38 mm na trnech lamp.

## [1.1.3] — 2026-09-05

### Changed

- UV: **sifon hadic a 1 m police kvůli elektřině zůstanou**; svislá tělesa ne. Položit lampy na polici, zásuvky nad nimi.

## [1.1.2] — 2026-09-05

### Added

- [lab.md](lab.md) — výtlak větve 1 ~2,5 m od dna pod skimmerem (statika od **hladiny**); větev 2: 1 m k UV. Lampy **položit naležato**, ne sifon nastojato.

## [1.1.1] — 2026-09-05

### Fixed

- [lab.md](lab.md) — kbelík 5. 9. 2026 byl při **čistých filtrech** a **zavřeném víru** (vše přes UV). 950 / 2 250 l/h jsou stropy 12 V, ne špína a ne krádež vírem.

## [1.1.0] — 2026-09-05

### Added

- [lab.md](lab.md) — kbelík 5. 9. 2026 (větev 1: 950 l/h, větev 2: 2 250 l/h), tmavě zelený až šedý zákal jako mrtvá řasa bez záchytu za UV.

## [1.0.2] — 2026-09-05

### Added

- [provoz.md](provoz.md) — CPF-10000 a třetí 55 W UV nekupovat; definice křemenky; vír krade průtok z UV, dokud není B na 4000–5500 l/h.
- [zapojeni.md](zapojeni.md) — do BOM fólie Firestone PondGard EPDM 1 mm, 7 bm × 9,15 m, nákup 12. 7. 2020 za 13 386 Kč.

### Fixed

- Terminologie: proud vody je **vír**, ne výr.
- Skimmer CSP-8000 je jen koš — v zapojení **není** 230 V čerpadlo 80 W / 10 000 l/h.

## [1.0.1] — 2026-09-05

### Added

- [zapojeni.md](zapojeni.md) — as-built popis větví, nákupní odkazy a odhad ceny k 5. 9. 2026.
- [solar.md](solar.md) — 12 V záloha as-built; plán 48 V sběrnice (Humsienk 5,12 kWh, izolovaný Orion 48/12, Phoenix 48/250) a FVE ~2 kWp na zimní vzduchování v Polabí.
- [provoz.md](provoz.md) — zeolit a uhlí jen jako krátká kúra (místo, pořadí NH₄ → uhlí bez Dyofixu); průzračnost pořád UV + buben.
- GitHub Action: při tagu `v*` složí [all_in_one.md](all_in_one.md) a pushne ho na `main`.

## [1.0.0] — 2026-09-05

První vydání provozního zapojení koupacího jezírka 40 m³ / 40 Koi.

### Added

- Větev 2: UV 2×55 W → netlakový buben (max. 6000 l/h) → Invital Biofiltr 550, vír jako obchoz.
- Diagnostika zákalu a kbelíkový test (cíl větve B 4000–5500 l/h).
- Umístění dvou měřičů (hlubina 0,7–1 m, výtok IBC).

### Fixed

- Hadice od Aquamax 12000: 50 mm k T-kusu, ne Y 2×40 mm.

### Removed

- Větší tlakový filtr na větvi 2, satelitní dnové sání, bazénový písek na 12 V, stálý zeolit a uhlí souběžně s Dyofixem.

[1.2.0]: https://github.com/fedurca/koi_koupaci_jezirko/releases/tag/v1.2.0
[1.1.5]: https://github.com/fedurca/koi_koupaci_jezirko/releases/tag/v1.1.5
[1.1.4]: https://github.com/fedurca/koi_koupaci_jezirko/releases/tag/v1.1.4
[1.1.3]: https://github.com/fedurca/koi_koupaci_jezirko/releases/tag/v1.1.3
[1.1.2]: https://github.com/fedurca/koi_koupaci_jezirko/releases/tag/v1.1.2
[1.1.1]: https://github.com/fedurca/koi_koupaci_jezirko/releases/tag/v1.1.1
[1.1.0]: https://github.com/fedurca/koi_koupaci_jezirko/releases/tag/v1.1.0
[1.0.2]: https://github.com/fedurca/koi_koupaci_jezirko/releases/tag/v1.0.2
[1.0.1]: https://github.com/fedurca/koi_koupaci_jezirko/releases/tag/v1.0.1
[1.0.0]: https://github.com/fedurca/koi_koupaci_jezirko/releases/tag/v1.0.0
