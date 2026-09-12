# GMT 3D Histogram — 3D Bar Histograms of Bathymetric Depths

GMT (Generic Mapping Tools) shell scripts that render three-dimensional bar histograms of bathymetric and topographic depth values. A relief grid is converted to an XYZ point table and drawn as 3D columns in a perspective view, visualising the spatial distribution of depths across an ocean trench. The scripts have been used to generate figures in the author's marine-geomorphological and cartographic publications.

## What the scripts do

- convert a bathymetry grid to an XYZ ASCII table (grd2xyz)
- inspect the depth / height range (gmtinfo)
- plot the data as 3D bars in perspective, with a controllable view azimuth and elevation (psxyz -So ... -p), a vertical (-JZ) axis and a base level
- add title, perspective annotation and the GMT logo (pstext, logo)
- export to raster (psconvert) at high resolution

## Data source

Global relief / bathymetry: ETOPO (5 arc-minute), converted to XYZ.

## Files

- GMT-23-3D-histogram.sh: 3D depth histogram of the Kuril-Kamchatka Trench
- GMT-23-3D-histogram-14J.sh: variant

## Requirements

- GMT 6.x (Generic Mapping Tools): https://www.generic-mapping-tools.org
- A POSIX shell (bash)
- A bathymetry grid (e.g. ETOPO) available locally

## Usage

Place the required bathymetry grid in the working directory, adjust the -R region, -p perspective and -JZ vertical scale at the top of the script, then run:

    bash GMT-23-3D-histogram.sh

The script writes a PostScript file and converts it to a raster image (JPG/PNG) via psconvert.

## Author and citation

Polina Lemenkova
ORCID: https://orcid.org/0000-0002-5759-1089

These scripts support figures in the author's marine-geomorphological and cartographic papers; please cite the specific article a given figure appears in. The full publication list is available via the ORCID record above.

## License

See the LICENSE file in this repository.
