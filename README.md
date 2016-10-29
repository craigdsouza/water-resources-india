# Water Resources of India
A simple webmap showing important layers made public by the [Water Resources Information System](http://www.india-wris.nrsc.gov.in/WMSServicesApp.html) (WRIS) (Central Water Commission of India)<br>
Click here to view: https://craigdsouza.github.io/water_resources_india/

![Preview showing river basins and command areas](/images/river-basins-and-command-areas.PNG)
Map of river basins and surface irrigation command areas (light yellow) in India, with a Mapbox light basemap.

## What is this project about?<br> 
The Central Water Commission of India makes available their maps in a WMS format [here](http://www.india-wris.nrsc.gov.in/WMSServicesApp.html)<br>
WMS => Web Map Services i.e. You can only view the map data but don't touch .. hence WMS != open data :)<br>

Despite the fact that the raw data behind the map is not openly released by CWC, the WMS format still has its advantages.<br>
They allow maps to be overlaid over other maps in the same format to understand how multiple features correlate.

There are in total 57 web maps made available. Some of these are more useful than others. This webmap puts together 18 of these layers to visualize in a simple format, using Leaftlet.js

The map layers include
* Administrative layers: State, District, Taluka, Village boundaries (2001 census)
* Hydrological layers: Rivers, Water bodies, Wetlands,River basins, Watersheds, Aquifers, Groundwater fluctuation, Groundwater depth
* Water Resource Development layers: Command areas, canals, dams, barrages/weirs/anicuts,planned interlinking of rivers projects,District wise Minor Irrigation Potential Created, District wise Groundwater Resource Status, District wise: dugwells,tubewells,lift schemes etc.

## How to use the map?
Click in the upper right corner of the webmap to see
* Multiple basemaps - Mapbox-light is the clutter free default basemap but Mapbox-satellite is also available. So is Open Street Map and NASA Night lights (just for fun!)
* Click checkboxes on/off to view any of 18 layers of your interest. Some may take longer to load. Some require you to zoom in before the map is visible.

## Why the need for this? Isn't it a replication of WRIS?
The Water Resources Information System (WRIS) is a great resource to have. It is certainly a big step forward from the level of access the average citizen enjoyed in the pre-digital era. However there are two reasons why I felt the need for something like this.<br>
1. The cumbersome interface -<br>The WRIS website interface is heavy on data usage and slow to load. Navigating around the website to find the layers we are interested in can also be a pain. A dedicated user may have the patience, but for the average website visitor this can be a frustrating exercise. Hence it made sense to develop a simplified Leaflet webmap that showed the most commonly accessed layers and loaded quickly. Moreover the webmap uses basemaps infinitely better than the basemaps used by WRIS<br>
2. Access to raw data -<br>A researcher is always going to be interested in the raw data. WRIS however does not make this available. I am hoping to make this web map into a editable webmap so users can digitize over the WMS for their own area of interest and then export the data (in kml/geojson/shp) for their own use.

![Map of Dams-Barrages-Weirs-Anicuts](/images/dams-barrages-weirs-anicuts.PNG)
Map of dams, barrages, weirs, anicuts in India, with a Mapbox satellite basemap

## How you can help?
* Do feel free to use and share the webmap as widely as you like. Would be especially good as a teaching resource
* If you want to explore other layers of the 57 layers made available by WRIS, then view the WRIS-Layers-Metadata.txt file in the repository to see WMS URLs for each of them.<br>
* Check out the code and improve on it.
* If you know anything about making editable geometries in Leaflet maps then mail me.. My id is craigds022@gmail.com

## Limitations of this webmap
* The WMS layers do not automatically generate a legend when a map is loaded. Hence some layers are not intuitive to read.<br>
You can still visit the WRIS website and navigate around to locate the legend you need.
* Very little metadata is made available by WRIS to explain how they generated the maps or even which year the maps correspond to.
* WMS maps do not allow you to change the colour scheme, fonts etc

## License
* This repository README and Metadata posts are under [Creative Commons – Attribution-ShareAlike 2.0 Generic](https://creativecommons.org/licenses/by-sa/2.0/?) (CC BY-SA 2.0).
* The data in the repository is under [Open Data Commons Open Database License](http://opendatacommons.org/licenses/odbl/summary/) (ODbL).
* The code is under [GNU GPL v3](https://tldrlegal.com/license/gnu-general-public-license-v3-(gpl-3))
