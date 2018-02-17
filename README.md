# KitsapParcelViewer
A clone of Kitsap County's Parcel viewer webapp built on the Mapbox GL platform. This project is still under active development.

See the live version here: http://thomasryan.xyz/Maps/KitsapParcelViewer/indexlayers.html

# Sources
The original Kitsap parcel viewer can be found here: https://psearch.kitsapgov.com/webappa/

The data used for this parcel viewer was pulled from here: https://spf.kitsapgov.com/dis/Pages/resources.aspx

# Purpose
This project is designed as a demo of what can be accomplished when you apply the Mapbox tool chain to a traditional GIS application like a parcel viewer.

# Features
* A Mapbox Parcel Viewer
* Togglable layers
* Click for popups with attribute data for the selected feature
* Search for parcels by street address
* Multiple basemaps
* 3D Buildings
* Ability to geolocate the user on request
* Scale bar
* Desktop first design with mobile support

# Roadmap
Currently search is implemented by flying to the spatial coordinates of a geocoded street address. 

I would like to add the ability to search based on presence of the searched string in the attributes of any parcel. Mapbox GL doesn't have the ability to search a layer's attributes and return all the results that match a query. You can filter out features in a layer that don't match a specific query, but filtering redraws the layer which is too slow to handle the number of features in this parcel layer and it's limited to just the features currently rendered in the window.

https://www.ovrdc.org/apps/mapbox-parcel-viewer.html

This project is similar to my own and offers the ability to search by parcel attributes by using another library to search through a JSON version of the parcel layers attributes. Rather than going directly to JSON I'd like to find a library that can search a GeoJSON copy of the parcel layer data and return the field that matches the query as well as the coordinates for that parcel.

My intent is for the next update to this project to offer a functional 'search-by-parcel-attribute' feature.
