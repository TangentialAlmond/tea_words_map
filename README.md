# Tea words map
Did you know that the words for "tea" across languages come from two main roots _cha_ and _te_? To visualize this linguistic phenomenon, we can plot the world map and color-code the countries by their words for tea.

For this world map, I used three main datasets:
1. Shape file where the countries are represented as polygons
2. List of countries and their commonly spoken language(s)
3. List of languages and their tea word origins

Using these three files, I plotted a world map with the countries color-coded by their tea word origin in `tea_words_map.ipynb` notebook. The code in the notebook hasn't been fully organized, but I hope it helps you to get the gist of how the world map was made for the SG Tea Friends parklet. 🌱

### Limitations
The datasets I've used here have the following limitations:
1. The shape file I use is a low resolution file using borders from 2009.
2. Many countries have more than one commonly spoken language and the dataset I use marks a language as `1` (commonly spoken) and `0` (not commonly spoken).
4. The names of the languages for the tea word origin and commonly spoken languages per country datasets do not always match.
5. The list of languages and their tea word origins is incomplete.

### Curious to know more?
Feel free to chat with one of the parklet volunteers! We're all tea nerds happy to chat. If you're curious about the coding aspect, feel free to look for Amanda.
