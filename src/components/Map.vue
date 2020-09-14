<template>
  <div class="map">
    <l-map class="map-container" style="height: 590px; z-index: 5;" :zoom="zoom" :center="center">
      <l-tile-layer :url="url"></l-tile-layer>
      <l-marker :lat-lng="markerLatLng">
        <l-popup>You!</l-popup>
      </l-marker>
    </l-map>
  </div>
</template>

<script>
import { LMap, LTileLayer, LMarker, LPopup } from "vue2-leaflet";
import { Icon } from "leaflet";

delete Icon.Default.prototype._getIconUrl;
Icon.Default.mergeOptions({
  iconRetinaUrl: require("leaflet/dist/images/marker-icon-2x.png"),
  iconUrl: require("leaflet/dist/images/marker-icon.png"),
  shadowUrl: require("leaflet/dist/images/marker-shadow.png")
});

export default {
  components: {
    LMap,
    LTileLayer,
    LMarker,
    LPopup
  },
  data() {
    return {
      url:
        "https://api.maptiler.com/maps/streets/256/{z}/{x}/{y}.png?key=e8LZc57PV2AwP7LJPKLT",
      zoom: 9,
      center: [4.0537386, 9.66443658],
      markerLatLng: [4.0537386, 9.66443658]
    };
  }
};
</script>

<style>
.map {
  z-index: 5;
}
.map-container {
  height: 100%;
}
</style>
