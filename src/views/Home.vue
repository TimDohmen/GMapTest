<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <h1>My First Google Map</h1>
    <div id="googleMap" style="width:100%;height:400px;"></div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld
  },
  mounted() {
    var mapProp = {
      center: new google.maps.LatLng(51.508742, -0.12085),
      zoom: 5
    };
    var map = new google.maps.Map(
      document.getElementById("googleMap"),
      mapProp
    );
  }
};
</script>
