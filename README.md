# Beyond the Manhattan Project

An interactive digital humanities map exploring how research, production, and nuclear testing sites across the United States helped build the American nuclear complex from the early years of nuclear research through the Cold War.

**[Explore the map](index.html) · [About the project](project.html)**

---

## About the project

The Manhattan Project is often associated with a few well-known places, including Los Alamos, Oak Ridge, and Hanford. This project looks beyond those landmarks to trace the wider geography of the nuclear complex: the universities and laboratories where research took place, the industrial sites that supported wartime production, and the facilities and communities affected by later nuclear testing and waste.

The map presents a curated selection of 19 locations. Each marker offers a short historical description, an image, and links to further reading and image credits. The goal is to make the geographic reach and lasting consequences of this history easier to explore while recognizing that the mapped sites are a starting point, not a complete inventory.

## Exploring the map

- **Browse locations:** Select a marker to read about a site's history and follow links to additional sources.
- **Move through time:** Use the timeline slider to reveal locations by their associated year, from 1931 to 1970.
- **Explore project themes:** The [project overview](project.html) introduces the map's focus on research, production, and consequences.

## Data and sources

The map's location records are embedded in the JavaScript in [`index.html`](index.html); there is no separate CSV or downloadable dataset. Each record includes a location name, latitude and longtitude, year, description, image, and links for further reading and image attribution. Images are stored in the [`images/`](images/) directory.

Historical descriptions and images draw on a range of linked sources, including government and institutional histories, archives, and Wikimedia Commons. Source and image-credit links are provided with the relevant map locations. The selection and summaries are intended as an introduction and should be read alongside the linked sources.


## Technology

- **HTML, CSS, and JavaScript** — page structure, styling, and location data
- **[Leaflet](https://leafletjs.com/)** — interactive map and markers (loaded from jsDelivr)
- **[Stadia Maps](https://stadiamaps.com/)** — map tiles, with attribution to OpenMapTiles and OpenStreetMap contributors
- **GitHub Pages** — suitable for static hosting; no build tools are required
