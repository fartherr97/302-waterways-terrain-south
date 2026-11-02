# 302 Waterways terrain tiles: south

Depth and elevation tiles for the 302 Waterways 3D view, served by GitHub Pages at
`https://fartherr97.github.io/302-waterways-terrain-south/`.

- Source: NOAA NCEI Continuously Updated Digital Elevation Model (CUDEM),
  1/9 arc-second topobathy (public domain).
- Area: the Atlantic coast south of 39.1°N outside the first region: Virginia (with the lower Chesapeake), North Carolina, South Carolina, Georgia and Florida's Atlantic side and the Keys.
- One of the sets listed in the first set's `sets.json`
  (`https://fartherr97.github.io/302-waterways-terrain/sets.json`); the app fetches a
  tile from the set whose core holds the middle of its zoom-10 tile.
- Tiles: XYZ (Web Mercator) at zoom 10, 12 and 14 (14 only where there is water);
  `index.json` lists them.
- Format: 257 × 257 int16 heights in decimetres (NAVD88), rows north → south, each row
  delta-coded (first value absolute), little-endian, gzip.

Built by `scripts/engine3d/bake_coast.py` and `split_sets.py` in the app repository.
