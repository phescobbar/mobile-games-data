# Mobile games data: App Store and Google Play facts for 8,047 games

Store facts for 8,047 iPhone and Android games, side by side: ratings and rating counts on both stores, Google Play downloads, prices, the Google Play "Contains ads" and "In-app purchases" labels, iPhone download size, languages, age rating, release and update dates, and US App Store chart positions.

It covers every game in the US App Store top charts for games (free, paid and top grossing, overall and for each game genre), every other game with 1,000+ US App Store ratings from the same studios, and the games on the [Boltshorts](https://boltshorts.com) lists. Last read from the stores on October 27, 2026.

**Browse it, with a page per game and benchmarks per genre:** https://boltshorts.com/data/

## At a glance

- 8,047 games, 36 columns, one row per game.
- 73% of the games we matched on Google Play carry the "Contains ads" label (4,005 of 5,522).
- 18% cost money up front on the App Store.
- Median App Store rating 4.64, median iPhone download 305 MB.

More findings: [Mobile game ads, prices and sizes: what the data says](https://boltshorts.com/mobile-games-by-the-numbers/).

## Files

| File | What it is |
|---|---|
| [`mobile-games.csv`](mobile-games.csv) | All games, every column |
| [`mobile-games.json`](mobile-games.json) | The same, as JSON, with the column dictionary |
| [`genres/`](genres/) | One CSV per App Store game genre (16 genres) |
| [`charts/`](charts/) | US App Store top 100 game charts for iPhone, one CSV per day |
| [`archive/`](archive/) | Every dated version of the table (3 so far), to follow ratings, prices and sizes over time |
| [`datapackage.json`](datapackage.json) | Frictionless Data descriptor |

## Columns

| Column | Meaning |
|---|---|
| `name` | Game name as we write it (the App Store name without the tagline). |
| `studio` | Developer shown on the App Store. |
| `released` | First release date on the US App Store. |
| `genre` | Main App Store category. |
| `ios_rating` | Average rating on the US App Store, exact to two decimals. |
| `ios_ratings` | Number of ratings on the US App Store. |
| `android_rating` | Average rating on the US Google Play store. |
| `android_ratings` | Number of ratings on the US Google Play store. |
| `android_downloads` | Download range shown by Google Play, for example 10M+. Blank when we could not match the game to a Google Play page. |
| `price_ios` | Price on the US App Store: Free, a dollar price, Free to try, Apple Arcade or Netflix membership. |
| `price_android` | Price on the US Google Play store. |
| `android_ads` | Whether the Google Play page shows the "Contains ads" label. |
| `android_iap` | Whether the Google Play page shows the "In-app purchases" label. |
| `ios_size_mb` | Download size on iPhone from Apple's iTunes Search API. |
| `ios_languages` | Number of languages listed on the App Store. |
| `ios_version` | Latest version number on the App Store. |
| `ios_last_update` | Date of the latest App Store update. |
| `age_rating` | Age rating on the US App Store. |
| `read_on` | Most recent date we read this game's store pages. |
| `app_store_url` | US App Store page. |
| `google_play_url` | US Google Play page. |
| `boltshorts_page` | This game's page on Boltshorts, with every number and how it compares. |
| `boltshorts_lists` | Boltshorts lists that rank this game. |
| `app_store_id` | Numeric App Store id. It never changes, so it is the key to join versions and other datasets. |
| `genres` | Every App Store category of the game, main one first, separated by semicolons. |
| `ios_min_version` | Oldest iOS version the current App Store build supports. |
| `ipad` | Whether the App Store lists iPad among the supported devices. |
| `ios_advisories` | Content descriptors behind the App Store age rating, for example "Loot Boxes" or "Infrequent/Mild Simulated Gambling". |
| `android_developer` | Developer name shown on Google Play. |
| `android_released` | Release date shown on Google Play. |
| `android_last_update` | Date of the latest update shown on Google Play. |
| `android_iap_range` | Price range per item that Google Play shows, for example "$0.99 - $99.99 per item". |
| `android_editors_choice` | Whether the Google Play page shows the Editors' Choice badge. |
| `chart_date` | Date of the App Store top charts in chart_positions. |
| `chart_positions` | Positions in the US App Store top 100 charts for iPhone on chart_date, as chart/category/rank, separated by semicolons. Categories are App Store game genres; "Games" is the chart of all games. |
| `source_set` | "boltshorts-lists" for a game on one of our lists, "app-store-charts" for a game that was in a US App Store top chart for games when we read them, "same-studio" for another game with 1,000+ US App Store ratings from a studio already in the table. |

## How it is collected

App Store facts come from the US App Store pages and Apple's iTunes Search API; Google Play facts from the US Google Play pages. A game is matched across the two stores only when the developer and the title agree (or the package name equals the App Store bundle id); when we are not sure, the Google Play columns stay blank instead of guessing. Store ratings are what each store shows on the read date. Details: https://boltshorts.com/data/#how

## License and citation

[CC BY 4.0](LICENSE). Use it for anything, credit "Boltshorts" with a link to https://boltshorts.com/data/.

> Boltshorts (2026). Boltshorts mobile games data [Data set]. https://boltshorts.com/data/. Read from the US App Store and Google Play on October 27, 2026.

Corrections: escobarbusinesslabs@gmail.com
