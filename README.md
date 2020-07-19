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

The following command returns the WOEID of the Canadian states.
```bash
$ q -t -H  "SELECT * FROM states.tsv WHERE ISO='CA' "
2344915 CA      Alberta ENG     State   23424775
2344916 CA      British Columbia        ENG     State   23424775
2344917 CA      Manitoba        ENG     State   23424775
2344918 CA      New Brunswick   ENG     State   23424775
2344919 CA      Newfoundland and Labrador       ENG     State   23424775
2344920 CA      Northwest Territories   ENG     State   23424775
2344921 CA      Nova Scotia     ENG     State   23424775
2344923 CA      Prince Edward Island    ENG     State   23424775
2344924 CA      Québec  FRE     State   23424775
2344925 CA      Saskatchewan    ENG     State   23424775
2344926 CA      Yukon Territory ENG     State   23424775
20069920        CA      Nunavut ENG     State   23424775
2344922 CA      Ontario ENG     State   23424775
```
