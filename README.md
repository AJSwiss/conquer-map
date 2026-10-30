# Conquer Map

A small browser-based 2D map that centers on your current location.

## Run locally

From this folder, start a local server:

```powershell
python -m http.server 8000
```

Then open `http://localhost:8000` in a browser and allow location access when prompted. The map uses Leaflet with OpenStreetMap tiles, and your coordinates are read only from the browser's Geolocation API.

The entire map is conquerable. The live location watcher updates while walking, and one buffered 20 m radius shape expands around the user's path. The continuously growing territory is stored locally in the browser.

Use **Test a simulated walk** in the territory panel to move through a short loop and watch the recording expand without moving the map viewport. The button can be stopped at any time. **Reset conquered territory** clears the saved shape and walking history.
