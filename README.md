# YuGiOhCardStatCorrelations
This was a project for my Data Visualization class. This shows a two-dimensional grid where the x and y-axes correspond to a user-selected stat (either ATK, DEF, or Level/Rank) on a [Yu-Gi-Oh! monster card](http://yugioh.wikia.com/wiki/Monster_Card). You can also select a color-scheme using the "Color" dropdown (which has no meaning relating to the data; it is purely an aesthetic effect).

By default, the grid will account for all monster cards, but you can filter which cards you want the grid to show by Attribute, Type, and Category. If you choose a value for any of these dropdowns, the grid will only show cards of that Attribute/Type/Category. Choosing values for multiple dropdowns will narrow the results further, as the cards must satisfy all filter criteria.

If you click on a cell, you'll see the monsters corresponding to that cell. ATK and DEF are rounded down to a multiple of 100. So if the x-axis is set to ATK and the y-axis is set to DEF, and you click the (10, 10) cell, you'll see all monsters (satisfying the current filter) with an ATK between 1000 and 1099 (inclusive) and a DEF between 1000 and 1099 (inclusive). Each monster has a link to their corresponding [Yu-Gi-Oh! Wikia](http://yugioh.wikia.com/wiki/Main_Page) page (although since these URLs are generated based on their name, some of the links are incorrect, but most of them work).

The data was scraped from [Yu-Gi-Oh! Card Guide](http://www.yugiohcardguide.com/) and transformed into a JavaScript literal list of objects. This was because there was a lot of data, and parsing it through code at run-time would be slow. This literal exists in a separate `.js` file, and is assigned to a variable, which is accessible through the main code.

The repo contains all necessary source code. A JSFiddle can be found [here](https://jsfiddle.net/3ebyg7yx/embedded/result/) for convenience.

Only the source code (not the data) is available through the MIT License in the `LICENSE` file. This application is not affiliated with Yu-Gi-Oh!, the Yu-Gi-Oh! Wikia, or the Yu-Gi-Oh! Card Guide.
