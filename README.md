# CFM 7.0 Fault Explorer

An interactive 3D viewer for the 608 triangulated fault surfaces in the SCEC Community Fault Model 7.0
(556 preferred, 39 alternative and 13 rupture representations). Built with three.js and runs entirely in the browser.

You can:

- orbit, zoom and pan around the 2000 m meshes
- filter by model set, slip sense and fault area
- colour by slip sense, depth or model set
- exaggerate the vertical scale from 1× to 10×
- search for any fault and click it to see its metadata

## Data

- **Fault model:** Plesch, A., Marshall, S. T., & Shaw, J. H. (2024). *SCEC Community Fault Model (CFM) 7.0*.
  Zenodo. https://doi.org/10.5281/zenodo.13685611. Released under the BSD 3-Clause License (see `LICENSE-DATA.txt`).
  The CFM authors ask that users also cite Plesch et al. (2007), *Bulletin of the Seismological Society of America*, 97(6), 1793–1802.
- **California outline:** US Census Bureau cartographic boundary file, 2023, 1:20,000,000.
- `data/*.mesh.json` hold the 2000 m t-surf meshes, converted from GOCAD TSurf.
  Coordinates are km in NAD27 / UTM zone 11N (EPSG:26711), offset by (400, 4000) km; `pos` is base64 Float32 xyz and `idx` is base64 Uint32 triangle indices.
- `data/faults.json` holds the per-fault metadata from `CFM7.0_Metadata.xlsx` and each fault's offsets into the mesh buffers.

The central and northern California faults added in CFM 7.0 are preliminary pending community evaluation.
The SCEC CFM authors have not reviewed or endorsed this viewer.
