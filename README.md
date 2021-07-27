# OSM Bright

A Mapbox GL basemap style showcasing OpenStreetMap.
It is using the vector tile
schema of [OpenMapTiles](https://github.com/openmaptiles/openmaptiles).

## Sprites Generation

The `dolomate/spritezero` docker image was used for sprite generation:
as described in [https://github.com/macteo/spritezero-docker](https://github.com/macteo/spritezero-docker)

```
mkdir -p data/sprites
cp -r icons data/sprites
docker run -it -e FOLDER=_svg -e THEME=sprite -v ${PWD}/data:/data dolomate/spritezero
```

Sprites are then moved toplevel.
