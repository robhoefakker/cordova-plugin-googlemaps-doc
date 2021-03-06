## Description

A LatLng is a point in geographical coordinates: latitude and longitude.
Latitude ranges between -90 and 90 degrees, inclusive. Values above or below this range will be clamped to the nearest value within this range.

```js
var latLng = new plugin.google.maps.LatLng(40.712216,-74.22655);
```

## Tips

PhoneGap-GoogleMaps-Plugin allows you to write very more simple format for LatLng class.
The below code works with (only) this plugin.
Because the JS code of this plugin just checks the `lat` and `lng` properties.
```js
map.animateCamera({
  target: {
    lat: 35.13,
    lng: 137.33
  },
  zoom: 15
});
```


***
# LatLng Class Reference
Method | Return value | Description
----|------|----
equals(other:LatLng) | Boolean | Return true if other position is as the same as this LatLng.
toString() | String  | Converts to string representation.
toUrlValue(precision?:number) | String  | Returns a string of the form "lat,lng" for this LatLng. We round the lat/lng values to 6 decimal places by default.

Property | Return value | Description
----|------|----
lat | Number | (Readonly)Returns the latitude in degrees.
lng | Number | (Readonly)Returns the longitude in degrees.
