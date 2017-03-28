# ElectionResultsMap
This is a simple election results viewer map, showing vote counts by precinct.
It was built off of the Alameda County, California elections results viewer map. Many thanks to Alameda County and Darren Venn in particular. The biggest change we made was to remove the live election results reporting, since we only needed to display the official results after they had been certified. We also tweaked colors, logos, and of course the obvious -- precinct boundaries and local elections that were being reported.
It uses the ESRI JS API, along with Boulder County Precinct boundary layers (polygons) held as ArcGIS Feature layers, as well as layers for the cities and the county boundary.
Following the pattern of Alameda County, in order to have fast response times when using the map, we created a separate file that contains the results, json2016G.json. When the map loads, these results are combined with the precinct layers, and the color and popup for each precinct is set -- these values come from the json2016G file. 
When you change to a new race, the results are reloaded for each polygon.
Here is a link to the current production map:
http://maps.bouldercounty.org/boco/ElectionResults2016/
## How can I use this code?
You should be able to use this code for your own county by creating your own precinct boundary, city and county outline layers, then modifying the contents of the json2016G.json file to use these layers and to contain your own results. You may also want to make some changes to the index.html file. It works well for both desktop and mobile. Note that you will need your precinctIDs in the ElectionResults.json file to match the precinctIDs held in your ESRI precinct boundaries feature layer.
## How can I contribute?
You can make some great contributions to this code simply by submitting pull requests! It is intended as a starting point, so that we don't all have to create our election results maps from scratch.
