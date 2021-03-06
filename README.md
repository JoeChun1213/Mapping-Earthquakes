## Objectives
The main aim of this project is to showcase the use of various interfaces in Javascript to map and visualize the earthquake and tectonic plates data across the geographical areas. The interfaces are tailor-made for the purpose of easy analysis and visualization.


## Project Overview
In this project, we use the Leaflet.js Application Programming Interface (API) to populate a geographical map with GeoJSON earthquake data from a URL. Each earthquake was visually represented by a circle and color, where a higher magnitude has a larger diameter and is darker in color. In addition, each earthquake has a popup marker that, when clicked, shows the magnitude of the earthquake and the location of the earthquake. 

## Resources
We used the Leaflet library to plot the data on a [Mapbox map](https://www.mapbox.com) through an API request and created interactivity for the earthquake data. We added the USGS URL for earthquake data by navigating to the USGS Hazards Program, clicking the Earthquakes link to open the Real-time Data Feeds link and scrolled down to "GeoJSON Summary" Feed. There, we clicked the [All Earthquakes](https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_week.geojson) link under the “Past 7 Days” heading

- **Data Source:** [majorAirports.json](/majorAirports.json), [torontoRoutes.json](/torontoRoutes.json), [torontoNeighborhoods.json](/torontoNeighborhoods.json)
- **Software:** JS, D3, Leaflet  

## Tasks in this project
- Retrieve data from a GeoJSON file.
- Make API requests to a server to host geographical maps.
- Populate geographical maps with GeoJSON data using JavaScript and the Data-Driven Documents (D3) library.
- Add multiple map layers to geographical maps using Leaflet control plugins to add user interface controls.
- Use JavaScript ES6 functions to add GeoJSON data, features, and interactivity to maps.
- Render maps on a local server.

## Summary  
### logicStep1.js
[logicStep1.js](/Earthquakes_past7days/static/js/logicStep1.js) maps all recorded earthquakes in the past seven days.  

### logicStep2.js  
As a first step in making the earthquake data more visually appealing, we added some styling to the earthquake data in [logicStep2.js](/Earthquakes_past7days/static/js/logicStep2.js) and varied the radius of each earthquake based on the magnitude.  

### logicStep3.js  
Although, the size of the earthquake data based on magnitude looks great, it’s hard to tell the difference between earthquakes within the same area. We come up with the idea to color-code the earthquakes based on magnitude. We, also, added the magnitude and location as a popup for each earthquake in [logicStep3.js](/Earthquakes_past7days/static/js/logicStep3.js).  

### logicStep4.js
[logicStep4.js](/Earthquakes_past7days/static/js/logicStep4.js) has the earthquake data as an overlay on both the Streets and Satellite tile layers, so users can turn the data on and off.  

### logicStep5.js  
The final piece we added to the map in [logicStep5.js](/Earthquakes_past7days/static/js/logicStep5.js) is a legend for the color range of the earthquakes. A legend provides information needed for the colors of the earthquakes to make sense to the viewer without having to click on each marker.

## Challenge Overview  
In this challenge, we added a third map style as an additional tile layer. We ,also, added tectonic plate GeoJSON data to the map to illustrate the relationship between the location and frequency of seismic activity and tectonic plates.To illustrate the severity of the earthquakes in relation to the tectonic plates, we logged in to GitHub and accessed the tectonic plate data from this [GitHub repository](https://github.com/fraxen/tectonicplates). We, also, made an API call to the tectonic plate data using d3.json(), and then added the data as an overlay to the map using the L.geoJSON() layer. In addition to the streets and satelliteStreets maps, we added a third map style of our choosing. All map styles were added to the base layer so that they showed up on the map to allow the user to change which layers are visible.

## Objectives
- Use d3.json() to get tectonic plate data and add the data using the L.geoJSON() layer.
- Style the tectonic plate LineString data to stand out on the map.
- Add the tectonic plate data as an overlay with the earthquake data.
- Add a third map style to allow the user to select from three different maps.

## Challenge Summary
For the challenge, a third map style is added to the [logic.js](/Earthquake_Challenge/static/js/logic.js) file and has the following:
- It is added to the baseMaps.
- When selected the map style is present on the map.
- The earthquake and tectonic data are present on the map style.<br/>

The tectonic data is added to the [logic.js](/Earthquake_Challenge/static/js/logic.js) file and has the following:  
- It is added to the overlay  
- It shows up on any map with the earthquake data by default.  
- The lines are styled in a bright dark color.<br/>
<br/>

Adding an overlay for the earthquakes and tectonic plates allows the viewer:
- to toggle off and on the earthquake data 
- to toggle off and on the tectonic data.  
<br/>
<br/>
<br/>
<br/>  

The streets map is the default map. The default setting will always show both sets of data, earthquakes and tectonic.
