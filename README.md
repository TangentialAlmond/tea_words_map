<h1 align="center">🗺️ Tea Words Map 🗺️</h1>

I created a world map visualizing the root origin of words for tea. Countries were color-coded based on the root origin of their words for tea of their most commonly spoken languages. This map was created for an exhibition at the SG Tea Friends parklet as part of the [Bold At Work's "Parking Day 2025"](https://www.instagram.com/p/DOsH_EikSqj/).

<img width="790" height="391" alt="Image" src="https://github.com/user-attachments/assets/a36ad212-ac8e-4089-a05a-e3bbe1eee64e" />

## 📍 Roadmap
Most languages have words for "tea" that trace back to two roots _cha_ and _te_. To visualize this linguistic phenomenon, I decided to:
### 1. Get a list of countries and their commonly spoken language(s)
- [x] Dataset A: Retrieve a dataset of countries (rows) and languages (columns) with "1" indicating "commonly spoken" and "0" indicating "not commonly spoken" from [this paper](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0267151).
### 2. Find the consensus root origin for the word(s) for tea per country
- [x] Dataset B: Retrieve a dataset of languages associated to their country of origin and their tea word root origin assignment from [this WALS dataset](https://wals.info/feature/138A#2/20.0/147.3).
- [x] Dataset C: Retrieve the shapes of countries from [Natural Earth Data](https://www.naturalearthdata.com/http//www.naturalearthdata.com/download/110m/cultural/ne_110m_admin_0_countries.zip).
- [x] Trim datasets A and B down to the countries in dataset C. The countries in dataset C depends on the map resolution used. In this case, I used a low-resolution map so many small countries like Singapore aren't actually in the dataset. The absence of these small countries has little effect on the visualization because these small countries won't be visible for the size of the print version of the Tea Words Map.
- [x] For each country, map the tea word origin(s). If a country has more than one commonly spoken language, the country will have more than one tea word origin. The consensus tea word origin is used for assigning the tea word origin for the country.
- [x] Check for cases where a country does not have a consensus tea word origin. Note: None were found in this case.
### 3. Visualize the countries across the world color-coded by tea word origin
- [x] Based on the assignment of tea word origin per country, visualize the country shapes in dataset C color-coded by tea word origin using `geopandas`.
### 4. Manually fix incorrect tea origin assignments
- [x] Manually fill in countries without a tea word origin assignment.
- [x] Manually correct countries with the wrong assignment.


### Limitations
The datasets I've used here have the following limitations:
1. Dataset C is a low resolution file of country shapes using borders from 2009.
2. Many countries have more than one commonly spoken language and the dataset I use marks a language as `1` (commonly spoken) and `0` (not commonly spoken). This binary annotation is only one way of indicating if a language is commonly spoken in the country or not. Another way would be based of the percentage of speakers in the country, which is a metric I would've have preferred to use for this project. Unfortunately, I did not have time to use this alternative metric.
4. The names of the languages for the tea word origin and commonly spoken languages per country datasets do not always match, resulting in a dropout of commonly spoken languages. This dropout happens as datasets A and B do not used a standardized identifier for languages.
5. The list of languages and their tea word origins i.e. dataset B is incomplete.
