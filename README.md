# Interactive-Advocacy-Map
This will have an image overlay of legislative districts, which when clicked on will pop-up an information box with legislators information.



<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="initial-scale=1.0, user-scalable=no">
    <meta charset="utf-8">
    <title>Ground Overlays</title>
    <style>
      html, body {
        height: 100%;
        margin: 0;
        padding: 0;
      }
      #map {
        height: 100%;
      }
    </style>
  </head>
  <body>
    <div id="map"></div>
    <script>
// This example uses a GroundOverlay to place an image on the map
// showing an antique map of Newark, NJ.

var LegislaticeOverlay;

function initMap() {
  var map = new google.maps.Map(document.getElementById('map'), {
    zoom: 13,
    center: {lat: 47.417, lng: -120.36}
  });

  var imageBounds = {
    north: 49.002231,
    south: 45.572168,
    east: -117.036497,
    west: -124.726926
  };

  LegislativeOverlay = new google.maps.GroundOverlay(
      'http://www.nwcua.org/assets_site/img/New-WA-Overlay.png',
      imageBounds);
  LegislativeOverlay.setMap(map);
}

    </script>
    <script src="https://maps.googleapis.com/maps/api/js?key=AIzaSyBypKa9BdTjp-gVx4ZNnFGkH4lEm69MEBQ &callback=initMap&signed_in=true" async defer>
    </script>
  </body>
</html>

