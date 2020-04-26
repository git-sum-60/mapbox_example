
<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <div id="map"></div>
  </div>
</template>

<style>
	body { margin: 0; padding: 0; }
	#map { position: absolute; top: 0; bottom: 0; width: 100%; height: 50% }
</style>

<script>
var mapboxgl = require('mapbox-gl/dist/mapbox-gl.js');


export default {
  data: function() {
    return {
      message: "Welcome to Vue.js!",
      places: [
        {}
      ]
    };
  },
  mounted: function() {
    mapboxgl.accessToken = '';
    var map = new mapboxgl.Map({
    container: 'map',
    center: [12.550343, 55.665957],
    zoom: 5,
    style: 'mapbox://styles/mapbox/streets-v11'
    });

    var marker = new mapboxgl.Marker()
    .setLngLat([12.550343, 55.665957])
    .addTo(map);

    var marker = new mapboxgl.Marker()
    .setLngLat([-78.8784, 42.8864])
    .addTo(map);


  },
  methods: {}
};
</script>


