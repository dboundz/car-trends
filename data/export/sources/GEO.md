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

- Totals: raw **1370** · kept **1316** · dropped **54**

- **Ferrari** (2026-09-14): raw 845, kept 826, dropped 19
  - SF90 Coupe: count=54, median_ask=479992, median_miles=2250
  - SF90 Spider: count=65, median_ask=614795, median_miles=905
  - 296 Coupe: count=62, median_ask=339938, median_miles=1484
  - 296 Spider: count=53, median_ask=418985, median_miles=916
  - 488 Coupe: count=77, median_ask=339900, median_miles=12062
  - 488 Spider: count=142, median_ask=418378, median_miles=10227
  - F8 Coupe: count=41, median_ask=479996, median_miles=6570
  - F8 Spider: count=101, median_ask=657995, median_miles=4166
  - 458 Coupe: count=27, median_ask=474900, median_miles=8080
  - 458 Spider: count=40, median_ask=554995, median_miles=8580
  - F430 Coupe: count=28, median_ask=276853, median_miles=19268
  - F430 Spider: count=50, median_ask=272349, median_miles=14045
  - 360 Modena: count=22, median_ask=154952, median_miles=25092
  - 360 Spider: count=41, median_ask=146298, median_miles=19062
  - 355 Berlinetta: count=7, median_ask=239995, median_miles=45416
  - 355 GTS: count=1, median_ask=399995, median_miles=27345
  - 355 Spider: count=10, median_ask=264677, median_miles=22250
  - 348 TS: count=4, median_ask=141450, median_miles=17776
  - 348 Spider: count=1, median_ask=125000, median_miles=None
  - 348 TB: count=0, median_ask=None, median_miles=None
  - 348 GTB: count=0, median_ask=None, median_miles=None
  - 348 GTS: count=0, median_ask=None, median_miles=None
- **McLaren** (2026-09-14): raw 154, kept 131, dropped 23
  - 600LT Coupe: count=20, median_ask=240294, median_miles=17616
  - 600LT Spider: count=13, median_ask=259498, median_miles=14480
  - 675LT Coupe: count=2, median_ask=394948, median_miles=545
  - 675LT Spider: count=2, median_ask=447192, median_miles=2290
  - 765LT Coupe: count=16, median_ask=724975, median_miles=8766
  - 765LT Spider: count=10, median_ask=864700, median_miles=12074
  - Artura Coupe: count=50, median_ask=190994, median_miles=2606
  - Artura Spider: count=18, median_ask=279250, median_miles=188
- **Lamborghini** (2026-09-14): raw 342, kept 332, dropped 10
  - STO Coupe: count=27, median_ask=499912, median_miles=4319
  - Performante Coupe: count=26, median_ask=371350, median_miles=13851
  - Performante Spider: count=7, median_ask=384500, median_miles=15325
  - SV Coupe: count=24, median_ask=850478, median_miles=12596
  - SV Spider: count=8, median_ask=1025388, median_miles=12621
  - SVJ Coupe: count=27, median_ask=1499990, median_miles=6328
  - SVJ Spider: count=8, median_ask=1565357, median_miles=16989
  - Murcielago Coupe: count=22, median_ask=536750, median_miles=9960
  - Murcielago Spider: count=18, median_ask=749995, median_miles=14491
  - Gallardo Coupe: count=35, median_ask=169990, median_miles=19099
  - Gallardo Spider: count=35, median_ask=133199, median_miles=21940
  - Temerario Coupe: count=30, median_ask=456018, median_miles=818
  - Revuelto Coupe: count=65, median_ask=689900, median_miles=643
- **Ford** (2026-09-14): raw 29, kept 27, dropped 2
  - 2005 GT: count=12, median_ask=674900, median_miles=8833
  - 2006 GT: count=15, median_ask=869675, median_miles=926
