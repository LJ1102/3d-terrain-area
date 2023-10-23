# 3D-TERRAIN-AREA ![license](https://img.shields.io/badge/license-MIT-blue) ![build status](https://img.shields.io/badge/build-passing-brightgreen) ![npm version](https://img.shields.io/badge/npm-0.1.0-red)

This package allows you to calculate the terrain area of arbitrary polygons on the GPU.
Per default it utilizes public domain DEM (digital eleveation map) data from the [Shuttle Radar Topography Mission](https://www2.jpl.nasa.gov/srtm/)
providing a resolution of 30m (1 arc second) but other, higher resolution data sources can be integrated. Due to the GPU accelerated aproach massive areas can quickly be measured, while not recommended there's a (significantly slower) CPU fallback for server-side usage.

## Usage

```js
import calculateTerrainArea from '3d-terrain-area';

let coordinates = [
  52.532311, 13.313880,
  52.534077, 13.328341,
  52.532922, 13.328461,
  52.530332, 13.314346
];

// basic usage
let area = await calculateTerrainArea(coordinates);

console.log(`Terrain area is ${area}m² or ${area*10.7639}ft²`);
```
