
<template>
    <div id="google-map" class="google-map"></div>
  </template>
  
  <script>
  export default {
    mounted() {
      // Initialize the Google Map
      const map = new google.maps.Map(document.getElementById("google-map"), {
        center: { lat: -37.8495, lng: 145.1090 },
        zoom: 14, // Adjust the initial zoom level
      });
  
      // Add a marker to the map
      const marker = new google.maps.Marker({
        position: { lat: -37.8495, lng: 145.1090 },
        map: map,
        title: "Deakin University, Burwood",
      });
    },
  };
  </script>
  
  <style scoped>
  /* Add any custom styles for your map container here */
  #google-map {
  height: 500px; /* Set a minimum height for the parent container */
}

.google-map {
  width: 80%;
  height: 50%; /* Adjust this percentage as needed for your design */
  margin: 0 auto;
}
  </style>