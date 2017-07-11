---
layout: post
title:  "George River Itinerary"
title_short: "George River"
date:   2017-07-11 11:00:00
categories: family
published: true
---

<style>

.gm-style-iw {
    color: #000;
}

</style>

<script src="https://maps.googleapis.com/maps/api/js?sensor=false&key=AIzaSyCulIxQY3H9eMRxGv_P276AfsqnVbdg05E" type="text/javascript"></script>

<div id="map" style="height: 700px; width: 900px;"></div>

<script type="text/javascript">
    var locations = [
      ['OK in a Pinch', 54.996278,-66.299400],
      ['Fredrickson Portage', 55.046565, -66.252451],
      ['Doublet Site', 55.082249, -66.126280],
      ['Wolf Scat Campsite', 55.072471, -65.896168],
      ['Lac Talon', 55.125803, -65.582285],
      ['T-Rex', 55.422779, -65.229092],
      ['The Crossing West', 55.478902, -65.072536],
      ['Big Burn', 55.652701, -65.079660],
      ['Portage North', 55.764841, -65.079403],
      ['High Bluff', 55.852095, -64.807835],
      ['Beach Pie', 56.050280, -64.757881],
      ['The Narrows', 56.225365, -64.722691],
      ['Sand Beach',  56.387541, -64.728184],
      ['High Cliff', 56.598153, -64.739170],
      ['Two Caribou', 56.791572, -64.883108],
      ['Wolf Beach #1', 57.091593, -65.361357],
      ['Hubbard', 57.227322, -65.283337],
      ['First Trout', 57.426932, -65.319385],
      ['Berry Hill', 57.614291, -65.541773],
      ['Big Bend', 57.841690, -65.630007],
      ['Wolf Beach #2', 58.093485, -65.699787],
      ['Helen\'s Falls', 58.167851, -65.807247],
      ['OK Cabin', 58.379219, -66.025515],
      ['Airstrip', 58.572773, -65.935221],
      ['Kangiqsualujjauc', 58.694603, -65.954361]
    ];

    var map = new google.maps.Map(document.getElementById('map'), {
      zoom: 7,
      fullscreenControl: true,
      scaleControl: true,
      center: new google.maps.LatLng(57.088515,-66.049805),
      mapTypeId: google.maps.MapTypeId.TERRAIN
    });

    var infowindow = new google.maps.InfoWindow();

    var marker, i;

    for (i = 0; i < locations.length; i++) {
      marker = new google.maps.Marker({
        position: new google.maps.LatLng(locations[i][1], locations[i][2]),
        map: map
      });

      google.maps.event.addListener(marker, 'click', (function(marker, i) {
        return function() {
          infowindow.setContent(locations[i][0]);
          infowindow.open(map, marker);
        }
      })(marker, i));
    }
  </script>
