# ElectionResultsMap
This is a simple election results viewer map, showing vote counts by precinct.
It uses the ESRI JS API, along with Alameda County ROV Precinct boundary layers (polygons) held as ArcGIS Feature layers, as well as layers for the cities and the county boundary.
In order to create fast response times when using the map, we created a separate file that contains the results, ElectionResults.json. When the map loads, these results are combined with the precinct layers, and the color and popup for each precinct is set. 
When you change to a new race, the results are reloaded for each polygon.
Here is a link to the current production map:
http://electionmaps.acgov.org
## How can I use this code?
You should be able to use this code for your own county by creating your own precinct boundary, city and county outline layers, then modifying the contents of the ElectionResults.json file to use these layers and to contain your own results. You may also want to make some small changes to the index.html file. It works well for both desktop and mobile (we found that on the night of the last election, around 80% of our users were viewing it on mobile devices). Note that you will need your precinctIDs in the ElectionResults.json file to match the precinctIDs held in your ESRI precinct boundaries feature layer. On the night of the election we set up a load job that created a new version of the ElectionResults.json file every time new results came in, so that, during the evening, users would see updated results in their browser.
## How can I contribute?
You can make some great contributions to this code simply by submitting pull requests! It is intended as a starting point, so that we don't all have to create our election results maps from scratch. Here are some ideas:
* Create a new version of the ElectionResults.json file - this file can probably be optimized to make it clearer to read
* Create a MapBox version! - This would be great! I originally wanted to do this in MapBox and geojson, but our layers were in ESRI format, so it was easier
* Create a Leaflet version!
