# Geography filter — Car Trends overview

**Scope: United States + Canada only.**

When building `index.html`, every daily listing CSV row is filtered before stats are computed.

## Keep

- Location (or notes) mentions USA / United States / U.S. / U.S.A.
- Location (or notes) mentions Canada / Canadian / trailing `CAN`
- US state name or 2-letter abbreviation (e.g. `Houston, TX`, `Granger, IA`)
- Canadian province name or abbreviation (e.g. `Kelowna, British Columbia, Canada`)

## Drop

- Europe / UK / UAE / other non-US/CA country codes or region names
- Empty location with no clear US/Canada hint in notes
- Ambiguous geography that cannot be confirmed as US or Canada

All counts, medians, and day-over-day deltas on the overview are recomputed from the filtered rows (summary JSON is not used for metrics).

## Latest run

- Totals: raw **1397** · kept **1333** · dropped **64**

- **Ferrari** (2026-09-15): raw 871, kept 852, dropped 19
  - SF90 Coupe: count=56, median_ask=479951, median_miles=2250
  - SF90 Spider: count=63, median_ask=614795, median_miles=867
  - 296 Coupe: count=62, median_ask=339900, median_miles=1251
  - 296 Spider: count=63, median_ask=419995, median_miles=876
  - 488 Coupe: count=83, median_ask=339988, median_miles=12165
  - 488 Spider: count=145, median_ask=417895, median_miles=10643
  - F8 Coupe: count=43, median_ask=471212, median_miles=6618
  - F8 Spider: count=101, median_ask=656995, median_miles=4192
  - 458 Coupe: count=28, median_ask=476950, median_miles=8080
  - 458 Spider: count=40, median_ask=554995, median_miles=9254
  - F430 Coupe: count=30, median_ask=254814, median_miles=20552
  - F430 Spider: count=49, median_ask=274708, median_miles=12978
  - 360 Modena: count=23, median_ask=159908, median_miles=22232
  - 360 Spider: count=42, median_ask=152404, median_miles=17560
  - 355 Berlinetta: count=7, median_ask=239995, median_miles=45416
  - 355 GTS: count=2, median_ask=384998, median_miles=33022
  - 355 Spider: count=10, median_ask=264677, median_miles=22250
  - 348 TS: count=4, median_ask=141450, median_miles=17776
  - 348 Spider: count=1, median_ask=125000, median_miles=None
  - 348 TB: count=0, median_ask=None, median_miles=None
  - 348 GTB: count=0, median_ask=None, median_miles=None
  - 348 GTS: count=0, median_ask=None, median_miles=None
- **McLaren** (2026-09-15): raw 154, kept 128, dropped 26
  - 600LT Coupe: count=20, median_ask=240298, median_miles=16067
  - 600LT Spider: count=14, median_ask=258749, median_miles=14772
  - 675LT Coupe: count=3, median_ask=379900, median_miles=11542
  - 675LT Spider: count=2, median_ask=447192, median_miles=2290
  - 765LT Coupe: count=16, median_ask=725350, median_miles=6406
  - 765LT Spider: count=7, median_ask=879400, median_miles=12074
  - Artura Coupe: count=49, median_ask=191498, median_miles=2357
  - Artura Spider: count=17, median_ask=289250, median_miles=214
- **Lamborghini** (2026-09-15): raw 325, kept 319, dropped 6
  - STO Coupe: count=30, median_ask=501042, median_miles=4319
  - Performante Coupe: count=24, median_ask=370240, median_miles=14094
  - Performante Spider: count=6, median_ask=392000, median_miles=21793
  - SV Coupe: count=20, median_ask=849989, median_miles=12596
  - SV Spider: count=8, median_ask=1025388, median_miles=12621
  - SVJ Coupe: count=27, median_ask=1400478, median_miles=7092
  - SVJ Spider: count=8, median_ask=1565357, median_miles=16989
  - Murcielago Coupe: count=19, median_ask=750000, median_miles=9960
  - Murcielago Spider: count=15, median_ask=799675, median_miles=14491
  - Gallardo Coupe: count=35, median_ask=169990, median_miles=19016
  - Gallardo Spider: count=33, median_ask=135599, median_miles=21202
  - Temerario Coupe: count=30, median_ask=456018, median_miles=818
  - Revuelto Coupe: count=64, median_ask=692019, median_miles=669
- **Ford GT** (2026-09-15): raw 47, kept 34, dropped 13
  - Gen 1: count=23, median_ask=779996, median_miles=1104
  - Gen 2: count=11, median_ask=1065000, median_miles=249
