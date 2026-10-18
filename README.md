# Islamabad Schools Navigation

A responsive, browser-based school navigation demo for Islamabad. It displays featured schools on an interactive Leaflet map and can calculate a driving route, distance, and estimated travel time from the visitor's current location.

## Features

- Interactive map with OpenStreetMap tiles and fallback map providers
- Featured school locations in Islamabad
- Browser geolocation (permission required)
- Driving route, distance, and estimated time using the public OSRM routing service
- Responsive layout for desktop and mobile screens
- No build step or package installation required

## Run locally

1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. Allow location access when prompted to use your current position.

For best results, serve the folder through a local web server because browsers may restrict geolocation on `file://` pages. If Python is installed, open a terminal in this folder and run:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Publish a public GitHub Pages link

1. Sign in to GitHub and create a **new public repository** named `islamabad-schools-navigation`.
2. Upload `index.html`, `README.md`, `LICENSE`, and `.gitignore` from this folder.
3. Open the repository's **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main` and folder `/(root)`, then click **Save**.
6. Wait for the deployment to finish. GitHub will show your public website URL in the Pages section. It usually looks like:
   `https://YOUR-USERNAME.github.io/islamabad-schools-navigation/`

## Customize the project

- **Schools:** Edit the `places` array in `index.html`. Each entry has `name`, `area`, `lat`, and `lng`.
- **Profile:** The profile currently displays Ahmad Hassan and ARID Number 24-ARID-2197, as supplied for this project. Review whether you want these details publicly visible before publishing.
- **Photo:** The page optionally loads `photo.jpg`. Add your own image file to the repository if you want a profile photo; otherwise, the built-in fallback avatar is used.
- **Map and routing:** This project uses public third-party services. Their availability, usage policies, and rate limits may change.

## Important notes

- School locations and coordinates are example entries and should be checked before relying on them for real-world navigation.
- Route distance and time are estimates and can change with the routing data. The displayed time is not a live traffic prediction.
- The browser may use a demo starting point if location permission is denied or unavailable.
- Leaflet, map tiles, and routing are loaded from external services, so an internet connection is required.
- Do not commit private keys, passwords, student IDs, or personal information to a public repository.

## Technology

HTML · CSS · JavaScript · [Leaflet](https://leafletjs.com/) · [OpenStreetMap](https://www.openstreetmap.org/) · [OSRM](https://project-osrm.org/)
