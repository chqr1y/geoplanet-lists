# geoplanet-lists
An ordered set of geoplanet ID (WOEID)

About WOEID
-----------
https://en.wikipedia.org/wiki/WOEID

This identifier is useful, among other things, to request the twitter api with a geographical coordinate.
Ex: https://developer.twitter.com/en/docs/trends/trends-for-location/api-reference/get-trends-place

Problem, the Yahoo API allowing to get this ID has stopped working several years ago.

So, to get WOEID identifiers, a dump of this API exists on archive.org :
https://archive.org/details/geoplanet_data_7.10.0.zip

Why this repository ?
---------------------

On this repository, I pushed subsets that seems useful to work more easily with this dataset.
For example, the file countries.tsv contains all countries with its associated WOEID:
```bash
$ wc -l countries.tsv 
247 countries.tsv
$ head countries.tsv
WOE_ID  ISO     Name    Language        PlaceType       Parent_ID
23424921        XS      "Spratly Islands"       ENG     Country 1
23424801        EC      Ecuador SPA     Country 1
23424811        GF      "Guyane Française"      FRE     Country 1
23424978        BF      "Burkina Faso"  ENG     Country 1
23424829        DE      Deutschland     GER     Country 1
23424819        FR      France  FRE     Country 1
23424863        KE      Kenya   ENG     Country 1
56042304        BL      "Saint-Barthélemy"      FRE     Country 1
23424945        SI      Slovenija       UNK     Country 1
```
