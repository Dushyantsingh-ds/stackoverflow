# How To Add Google Maps With A Marker to a Website
Last Updated: 27-09-2020
Google Maps is a web mapping service developed by Google. It offers satellite imagery, street maps, 360° panoramic views of streets (Street View), real-time traffic conditions (Google Traffic), and route planning for traveling by foot, car, bicycle (in beta), or public transportation.
## To add a Google Maps with a marker on a website there are three essential steps required:

- Create an HTML page
- Add a map with a marker
- Get an API key

## Step 1 : Creating an Html page.

### Code
```
<!DOCTYPE html> 
<html> 
  <head> 
    <style> 
      #map { 
        width: 100%; 
        height: 400px; 
        background-color: grey; 
      } 
    </style> 
  </head> 
  <body> 
    <p>My Google Maps Demo</p> 
    <div id="map"></div> 
  </body> 
</html> 
```
### Output :
![alt text](https://media.geeksforgeeks.org/wp-content/uploads/Screen-Shot-2017-11-07-at-2.32.27-PM.png)

The given code describes the CSS that sets the size and color of the div. The style element sets the div size for your map.div is set to a height of 400 pixels, and width of 100% to display the map across the width of your web page.

```
<style>
#map {
width: 100%;
height: 400%;
background-color: grey;
}
</style>
```
The code defines an area of the page for the Google map. The div appears as a grey block in the output, because the map has not been yet added.
``` <div id="map"></div> ```
## Step 2 : Adding map with a marker :
### Code 
``` <!DOCTYPE html> 
<html> 
  <head> 
    <style> 
      #map { 
        height: 400px; 
        width: 100%; 
       } 
    </style> 
  </head> 
  <body> 
    <p>My Google Maps Demo</p> 
    <div id="map"></div> 
    <script> 
      function initMap() { 
        var test= {lat: -25.363, lng: 131.044}; 
        var map = new google.maps.Map(document.getElementById('map'), { 
          zoom: 4, 
          center: test 
        }); 
        var marker = new google.maps.Marker({ 
          position: test, 
          map: map 
        }); 
      } 
    </script> 
    <script async defer 
    src= 
"https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap"> 
    </script> 
  </body> 
</html> 
```
### Explanation :
-In the code , the script loads the API from the specified URL.
-The callback parameter executes the initMap function after the API loads.
-The async attribute allows the browser to continue rendering the rest of the page while the API loads.
-The key parameter contains the API key.
-Type your api key inside “key = “.
``` <script async defer scr="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY &callback=initMap">
</script> ```
<!-- The code contains the initMap function that initializes and adds the map when the web page loads.Script tag can be used to add your own javascript. -->
``` <script
function initMap() {
var test = {lat: -25.363, lng: 131.044};
var map = new
```
-The code constructs a new Google maps object, and adds properties to the map including the center and zoom level.
-In the code below, new google.maps.Map() creates a new Google maps object.
-The center property tells the API where to center the map. The map coordinates are set in the order: latitude, longitude.
-The zoom property specifies the zoom level for the map. Zoom: 0 is the lowest zoom, and displays the entire earth. Set the zoom value higher to zoom in to the earth at higher resolutions.

``` var test = {lat: -25.363, lng:131.044};
var map = new
google.maps.Map(document.getElementById('map'),{
zoom: 4,
centre: test
}); 
```
The code below puts a marker on the map. The position property sets the position of the marker.
```
var marker = new google.maps.Marker({
position: uluru,
map: map
});
```
## Step 3: Getting an API key
### Following are the steps required to get a API key:

-Go to the below mentioned link
https://console.developers.google.com/flows/enableapi?apiid=maps_backend,geocoding_backend,directions_backend,distance_matrix_backend,elevation_backend,places_backend&reusekey=true.
-Create a new project or select from your existing projects.
-Click Continue to enable the API.
On the Credentials page, get an API key (and set the API key restrictions).
Replace the value of the key parameter in the URL with your own API key
### Output :
![alt text](https://media.geeksforgeeks.org/wp-content/uploads/Screen-Shot-2017-11-07-at-4.15.14-PM.png)

## Add GeeksforGeeks office City

### INPUT :
```
<!DOCTYPE html> 
<html> 
<head> 
	<style> 
	#map { 
		height: 400px; 
		width: 100%; 
	} 
	</style> 
</head> 
<body> 
	<h3>GFG Google Maps Demo</h3> 
	<div id="map"></div> 
	<script> 
	function initMap() { 
		var uluru = {lat: 28.501859, lng: 77.410320}; 
		var map = new google.maps.Map(document.getElementById('map'), { 
		zoom: 4, 
		center: uluru 
		}); 
		var marker = new google.maps.Marker({ 
		position: uluru, 
		map: map 
		}); 
	} 
	</script> 
	<script async defer 
	src= 
"https://maps.googleapis.com/maps/api/js?key= 
AIzaSyB2bXKNDezDf6YNVc-SauobynNHPo4RJb8&callback=initMap"> 
	</script> 
</body> 
</html> 
```
### Output
![alt text](https://media.geeksforgeeks.org/wp-content/uploads/Screen-Shot-2017-11-08-at-3.07.50-PM.png)



