# TransitPoint – Find Public Transport Near You

**TransitPoint** is a web-based public transport accessibility finder designed to help students, commuters, and people exploring unfamiliar locations discover nearby public transport stops. Users can search for a location, explore nearby stops on an interactive map, filter transport options, view stop details, and access walking directions.

The project uses OpenStreetMap data and web technologies to make finding nearby public transport simpler and more convenient.

## Features

- **Location Search:** Search for a place or address to find nearby public transport stops.
- **Current Location:** Use browser geolocation to search around your current position.
- **Interactive Map:** Explore nearby stops using a Leaflet map powered by OpenStreetMap.
- **Transport Filters:** Filter results by available public transport types.
- **Stop Information:** View details about individual stops through map markers and result cards.
- **Walking Directions:** Open an external map service to get walking directions to a selected stop.
- **Saved Stops:** Save preferred stops using browser storage for convenient access.
- **Input Validation:** Prevent empty or invalid location searches.
- **User Feedback:** Display loading indicators, status messages, error messages, and empty-result states.
- **Responsive Interface:** Use the application across desktop and mobile screen sizes.

## Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Structure and semantic elements of the web application |
| Tailwind CSS | Styling and responsive user interface |
| JavaScript | Application logic, events, validation, and interaction |
| Leaflet.js | Interactive maps and markers |
| OpenStreetMap | Map tiles and geographic data |
| Nominatim API | Convert location names and addresses into geographic coordinates |
| Overpass API | Retrieve nearby public transport stops and related map features |
| Fetch API | Send HTTP requests and retrieve API responses |
| JSON | Process geographic and transport data |
| Browser Geolocation API | Obtain the user's current coordinates with permission |
| Web Storage API | Save preferred stops in the browser |

## How It Works

1. The user enters a location or chooses to use their current location.
2. The application validates the input before beginning the search.
3. The Nominatim API converts the entered place or address into latitude and longitude coordinates.
4. The Overpass API retrieves available public transport features around the selected coordinates.
5. The application processes the returned JSON data and displays the available stops on the interactive map and in result cards.
6. Users can filter the results, select a stop to inspect its details, save preferred stops, or open walking directions.

The application searches within a configured radius of approximately **3 km** around the selected location. Distances displayed by the application are straight-line estimates, not actual walking distances.

## Getting Started

### Prerequisites

- A modern web browser.
- Visual Studio Code or another code editor.
- An active internet connection.
- The **Live Server** extension in Visual Studio Code, or another local web server.

### Installation

**1. Clone the repository**

Replace `YOUR_USERNAME` with your GitHub username.

```bash
git clone https://github.com/YOUR_USERNAME/TransitPoint.git
```

**2. Open the project folder**

```bash
cd TransitPoint
```

Open the folder in Visual Studio Code.

**3. Start the application**

Open the main HTML file and select **Open with Live Server**.

Alternatively, serve the project using another local web server.

**4. Explore TransitPoint**

- Enter a place or address in the search field.
- Submit the search.
- Select a transport filter if needed.
- Explore the results on the map and in the stop cards.
- Select a stop to view its details.
- Save preferred stops or open walking directions.

## APIs and Data Sources

### Nominatim API

Nominatim is used for geocoding. It searches for a location based on the user's text input and returns geographic coordinates and location information.

### Overpass API

The Overpass API queries OpenStreetMap data for nearby public transport features, such as bus stops, railway stations, and other supported transport locations.

### OpenStreetMap

OpenStreetMap provides geographic map data used to display the surrounding area and transport locations.

**Note:** API availability and data completeness may vary. The application requires an internet connection to retrieve map and transport information. Browser geolocation requires the user's permission and an appropriate browser context.

## Limitations

- Live bus or train arrival times are not provided.
- The availability and accuracy of transport stops depend on OpenStreetMap data and API responses.
- Search results may vary depending on location and data coverage.
- Displayed distances are straight-line estimates rather than road-network distances.
- Saved stops use browser storage and are not synchronised across devices or browsers.
- Walking directions are provided through an external mapping service.

## Future Enhancements

- Integration of real-time public transport arrival information where data sources are available.
- Route planning between an origin and destination.
- More detailed accessibility information for transport stops.
- Additional transport filters and improved search suggestions.
- Network-based walking distances and estimated travel times.
- User accounts and synchronised saved locations.

## Project Objective

The objective of TransitPoint is to improve access to public transport information by combining location search, open geographic data, interactive mapping, and simple user controls in a single web application.

## Data Attribution

Map data © [OpenStreetMap contributors](https://www.openstreetmap.org/copyright).

The application uses the [Nominatim API](https://nominatim.org/) for geocoding and the [Overpass API](https://overpass-api.de/) for querying OpenStreetMap data.

## Author

Developed as a web development project focused on public transport discovery and location-based services.
