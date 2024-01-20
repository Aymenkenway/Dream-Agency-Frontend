<!-- MapComponent.vue -->

<template>
  <div>
    <div ref="map" style="height: 300px"></div>
  </div>
</template>

<script>
import L from 'leaflet'
import 'leaflet/dist/leaflet.css'

export default {
  name: 'MapComponent',
  mounted() {
    // Initialize the map
    this.map = L.map(this.$refs.map).setView([35.541694, 6.163889], 13)

    // Add a tile layer (e.g., OpenStreetMap)
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '© Originova office',
    }).addTo(this.map)

    // Add a marker
    L.marker([35.541694, 6.163889]).addTo(this.map).bindPopup('Originova')
  },
}
</script>

<style scoped></style>
