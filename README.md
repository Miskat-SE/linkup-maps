# LinkUp offline maps

Maps for [LinkUp](https://github.com/Miskat-SE), the Android app for chatting and sharing files with people nearby without internet.

Download a map once while you have internet: in LinkUp, open **Settings → Offline maps**. After that it works anywhere, with no signal, and you can give it to people nearby from a chat (**Attach → Offline map**).

## Maps

**Light map** (the whole country, small):

| Map | Size | Contents |
|---|---|---|
| Bangladesh (`bd-light`) | 2.3 MB | Coast, rivers, divisions, districts, 134 towns, and the Bay of Bengal |

**Detailed maps**, one per division: roads, buildings, places and points of interest, drawn like Google Maps, with English labels and offline search.

| Map | Size |
|---|---|
| Barishal division (`bd-barishal`) | 11.1 MB |
| Chattogram division (`bd-chattogram`) | 41.9 MB |
| Dhaka division (`bd-dhaka`) | 42.5 MB |
| Khulna division (`bd-khulna`) | 31.2 MB |
| Mymensingh division (`bd-mymensingh`) | 15.9 MB |
| Rajshahi division (`bd-rajshahi`) | 19.0 MB |
| Rangpur division (`bd-rangpur`) | 34.7 MB |
| Sylhet division (`bd-sylhet`) | 16.8 MB |

Each [release](https://github.com/Miskat-SE/linkup-maps/releases) holds the maps (`.lmap` files) and `catalog.json`, the list the app reads from `releases/latest/download/catalog.json`. The app checks the size and SHA-256 of every map it downloads.

`.lmap` is LinkUp's own light vector format (gzip-compressed JSON), so maps stay small and follow the app's light and dark colours. Detailed maps are `.pmtiles` archives of OpenStreetMap vector tiles, with a search index in their metadata. The format and the tool that builds these maps are in the app's repository (`tool/maps/`).

## Data and licences

| Data | Source | Licence |
|---|---|---|
| Land, lakes, rivers | [Natural Earth](https://www.naturalearthdata.com) 1:10m | Public domain |
| Division and district borders | [geoBoundaries](https://www.geoboundaries.org) gbOpen BGD ADM1/ADM2, from the Bangladesh Bureau of Statistics and OCHA ROAP | [CC BY 3.0 IGO](https://creativecommons.org/licenses/by/3.0/igo/) |
| Towns and populations | [GeoNames](https://www.geonames.org) | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Bangla town names (light map) | Natural Earth populated places | Public domain |
| Detailed maps: roads, buildings, places, points of interest | [OpenStreetMap](https://www.openstreetmap.org/copyright) contributors, via the [Protomaps basemap](https://protomaps.com) | [ODbL 1.0](https://opendatacommons.org/licenses/odbl/) |

Every map credits these sources, and LinkUp shows the credit on the map. The detailed maps are a database derived from OpenStreetMap and are offered under the ODbL. Borders are for navigation only and are not an authority on international boundaries.
