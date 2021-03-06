# map.clear()

Removes all markers, polylines, polygons, overlays, etc from the map.

```html
<div class="map" id="map_canvas">
    <span class="smallPanel"><button>Click here</button></span>
</div>
```

```js
var div = document.getElementById("map_canvas");
var map = plugin.google.maps.Map.getMap(div);
map.one(plugin.google.maps.event.MAP_READY, function() {

  var button = div.getElementsByTagName('button')[0];
  button.addEventListener('click', function() {
    // Removes the markers completely.
    map.clear();
  });

  // Puts ramdom markers on the map.
  createMarkers(map);
});
function createMarkers(map) {
  map.getVisibleRegion(function(latLngBounds) {
    var sw = latLngBounds.southwest;
    var ne = latLngBounds.northeast;
    var diffY = (ne.lat - sw.lat);
    var diffX = (ne.lng - sw.lng);
    for (var i = 0; i < 100; i++) {
      map.addMarker({
        'position': {
          'lat': sw.lat + diffY * Math.random(),
          'lng': sw.lng  + diffX * Math.random()
        }
      });
    }
  });
}
```

![](image.gif)
