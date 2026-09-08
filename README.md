# Elder Care Homecare — Locations Map

A static page (`index.html`) showing a single interactive map (Leaflet + OpenStreetMap) with a
dot for each of the 12 Elder Care Homecare offices, plus a grouped sidebar list with "Get
Directions" links. Clicking a sidebar entry flies the map to that office's pin.

Location names and addresses are sourced from Elder Care Homecare's verified Google Business
Profile listings. Coordinates are not hardcoded — the page geocodes each address client-side via
OpenStreetMap's free Nominatim API when it loads (rate-limited to ~1 request/sec per Nominatim's
usage policy), so pin accuracy comes from that service, not from guesswork.

To update a location, edit the `locations` array in `index.html`.
