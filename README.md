# findposter

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A web application to find and visualize election poster locations and polling stations in Japan using Open Data and Google Maps.


![findposter screenshot](http://fukuno.jig.jp/2014/findposter.jpg)


## Features

-   Visualize locations of election posters and polling stations on an interactive map.
-   Automatically find nearby locations using your device's geolocation.
-   Navigate between the nearest points of interest with "Previous", "Next", and "Nearest" controls.
-   Fetches data from Japan's Open Data Platform (ODP) using SPARQL.

## Getting Started

### Prerequisites

This project requires a Google Maps API key to function. You must obtain a key and set it as the `API_KEY` variable in the `lib/gmap.js` file.

```javascript
// lib/gmap.js
var API_KEY = "YOUR_GOOGLE_MAPS_API_KEY_HERE";
```

### Running the Application

1.  Clone the repository to your local machine.
2.  Add your Google Maps API key to `lib/gmap.js` as described above.
3.  Open the `index.html` file in your web browser.
4.  The application will request your location to display the nearest points of interest.

## Data Source

This project retrieves data from the Open Data Platform (ODP) Japan via its public SPARQL endpoint.

-   **Endpoint:** `https://sparql.odp.jig.jp/data/sparql`
-   **Data Types Queried:**
    -   `http://odp.jig.jp/odp/1.0#PosterPlace` (Election Poster Locations)
    -   `http://odp.jig.jp/odp/1.0#Polls` (Polling Stations)

## Attribution

Based on the original work by Taisuke Fukuno.
> (c)taisukef CC BY http://fukuno.jig.jp/

## License

MIT License — see [LICENSE](LICENSE).