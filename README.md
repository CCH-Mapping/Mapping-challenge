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
All location records are embedded in the `dataset` array in [`index.html`](index.html); there is no separate data file. Each entry is a point feature with a `geometry` object and a `properties` object.

| Field | Type | Notes |
| --- | --- | --- |
| `type` | string | Feature type; use `Feature` |
| `geometry.type` | string | Geometry type; use `Point` |
| `properties.title` | string | Location name shown on the map |
| `geometry.coordinates` | number pair | Coordinates in `[longitude, latitude]` order, in decimal degrees |
| `properties.year` | integer | Year associated with the location; the timeline shows locations up to the selected year |
| `properties.description` | string | Historical context displayed in the marker popup; may include HTML links |
| `properties.image` | string | Path to the image in `images/` |
| `properties.alt` | string | Alternative text describing the image |
| `properties.figcaption` | string | Image credit or attribution displayed in the popup; may include HTML links |
| `properties.read` | string | URL for further reading about the location |
| `properties.icon` | object | Leaflet icon settings: `iconUrl`, `iconSize`, `iconAnchor`, and `popupAnchor` |

To add a location, append another feature to the `dataset` array and add its image to `images/`. Keep the coordinates in longitude-latitude order and provide the fields above. The timeline currently spans 1931–1970; update its `min` or `max` in `index.html` if a new location falls outside that range.

Historical descriptions and images draw on a range of linked sources, including government and institutional histories, archives, and Wikimedia Commons. Source and image-credit links are provided with the relevant map locations. The selection and summaries are intended as an introduction and should be read alongside the linked sources.



## Build with

- **HTML, CSS, and JavaScript** — page structure, styling, and location data
- **[Leaflet](https://leafletjs.com/)** — interactive map and markers (loaded from jsDelivr)
- **[Stadia Maps](https://stadiamaps.com/)** — map tiles, with attribution to OpenMapTiles and OpenStreetMap contributors
- **GitHub Pages** — suitable for static hosting; no build tools are required

## Repository Structure

index.html            landing page: title, intro modal, slider bar, and the map container
project.html.         project description page
img/                  one image per location, named to match its entry in locations.json
