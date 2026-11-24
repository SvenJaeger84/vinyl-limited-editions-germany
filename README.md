# Limited vinyl editions in German shops: prices, run sizes, colours

Aggregated figures on limited and coloured vinyl pressings sold by German online shops, compiled by
[VinylWelten](https://vinyl.vergleichswelten.de/), a price comparison site for limited vinyl editions.

**As of 2026-11-24.** 6696 editions in the catalogue, daily price measurements since 2026-10-15.

## Key figures

- A limited edition costs **30.87 euros** at the cheapest shop (median).
- When several shops sell the same edition, the gap between the most expensive and the cheapest offer is
  **3.08 euros** on average (7.31 percent).
- **70.1 percent** of the editions with a published run size are limited to 500 copies or fewer.
  The most common run is 500 copies, the smallest 18.
- **37.1 percent** are reissues; the original album is 20 years old in the median.
- **84.2 percent** of the editions are sold new by two or more shops. Where the prices differ,
  the cheapest shop saves **3 euros** in the median against the second cheapest.
- **50.2 percent** of the editions cost less than 30 euros at the cheapest shop.

## Files

| File | Content | Rows |
|---|---|---|
| `data/summary.csv` | Key figures in one place | 23 |
| `data/price_index_daily.csv` | Daily price index and median prices, overall and by genre and format | 762 |
| `data/run_sizes.csv` | Distribution of published run sizes | 5 |
| `data/pressing_colours.csv` | Pressing colours, grouped | 10 |
| `data/packaging_extras.csv` | Packaging features such as gatefold, insert, numbering | 10 |
| `data/releases_per_month.csv` | Limited editions by release month, twelve months back and announced months ahead | 16 |
| `data/genres.csv` | Editions by genre | 12 |
| `data/top_labels.csv` | Labels with the most limited editions | 25 |
| `data/price_ranges.csv` | Editions by price range (cheapest new price) | 8 |
| `data/shops_per_edition.csv` | Number of shops offering an edition new | 3 |
| `data/release_countries.csv` | Release country (EU-wide, USA, UK, Germany etc.) | 8 |
| `data/top_artists.csv` | Artists with the most limited editions | 12 |
| `data/reissue_decades.csv` | Reissues by decade of the original album release | 8 |

All files are UTF-8 CSV with a header row and a comma as separator. Prices are in euros including VAT, without shipping.

## Method

- **Catalogue:** limited vinyl editions that have a cover image and at least one shop offer. Product data comes from
  the affiliate feeds of the shops EMP, HHV and Thalia, complemented by Discogs.
- **Prices:** recorded every morning after the feeds are synchronised. For each edition the best price counts, that is
  the cheapest offer for new goods across all shops. Used records are excluded.
- **Price index:** a chained Jevons index. For each day it is the geometric mean of the price changes of all editions
  that had a price on both days. Editions that appear or sell out do not move the index. Base 100 = 2026-10-15.
- **Outliers:** daily changes of more than two thirds are discarded as feed errors.
- **Small groups:** segments with fewer than 30 editions are not reported.
- **Colours:** the shops state colours as free text. They are mapped to colour groups; patterns such as splatter or
  marble count as multi-coloured. Shops rarely state black explicitly, so black pressings are under-represented and no
  share of coloured pressings is given.
- **Reissues:** editions whose original album was first released at least two years before the pressing.
  `reissue_decades.csv` counts only these reissues, by the decade of the original release.
- **Shops per edition:** shops with a price for new goods on the day of the export. The saving compares the cheapest
  and the second cheapest shop and only counts editions where the two prices differ.
- **Release country:** as stated on Discogs, spelling variants merged (EU and Europe count as Europe).
- **Artists:** compilations by various artists are not counted.

## Limits

The figures describe this catalogue, not the whole record market. The focus is on rock and metal; jazz and classical
music are weakly represented. Not every edition has every attribute, so shares always refer to the editions with that
attribute. The dataset contains aggregated figures only: no individual shop prices and no product data from the feeds.

## Updates and current figures

The live tables are on the website, in German:

- Vinyl in Zahlen (colours, run sizes, prices, shops, packaging, genres, artists, labels, countries, releases): https://vinyl.vergleichswelten.de/vinyl-in-zahlen
- Vinyl-Preisindex (prices by genre and format, index history): https://vinyl.vergleichswelten.de/vinyl-preisindex

## Licence and citation

The data is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You may use it freely if you
name the source and link to it, for example:

> Source: VinylWelten, limited vinyl editions in German shops, as of 2026-11-24, https://vinyl.vergleichswelten.de/vinyl-in-zahlen

## Deutsch

Ausgewertete Kennzahlen zu limitierten und farbigen Vinyl-Pressungen bei deutschen Onlinehändlern, zusammengestellt von
VinylWelten, einem Preisvergleich für limitierte Vinyl-Editionen. Stand 2026-11-24, 6696 Editionen im Katalog,
tägliche Preismessung seit 2026-10-15.

Der Datensatz enthält nur zusammengefasste Werte: Median-Preise und Preisindex nach Genre und Format, die Verteilung von
Auflagen, Preisspannen, Pressfarben und Ausstattung, die Zahl der Händler je Edition, das Veröffentlichungsland,
Neuerscheinungen pro Monat, Neuauflagen nach Jahrzehnt, Genres sowie die Interpreten und Labels mit den meisten Editionen.
Einzelne Händlerpreise und Produktdaten aus den Feeds sind nicht enthalten. Gemessen wird der Katalog von VinylWelten,
nicht der gesamte Schallplattenmarkt.

Die Daten stehen unter der Lizenz CC BY 4.0 und dürfen mit Quellenangabe und Link frei verwendet werden.
