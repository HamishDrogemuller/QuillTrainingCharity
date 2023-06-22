<template>
    <div class="map-container">
      <div id="map"></div>
    </div>
  </template>
  
  <script>
    import { onMount } from 'svelte';
  
    export let Map;
  
    onMount(() => {
      const map = new google.maps.Map(document.getElementById('map'), {
        center: { lat: -41.27520, lng: 173.28912 }
      });
    });
  </script>
  
  <style>
    .map-container{
      width: 75%;
      height: 75%;
    }
  </style>

<head>
    <script src="https://maps.googleapis.com/maps/api/js?key=AIzaSyDx8LN58Ol5Td4iSjtjgtTkGhqNwV8B8Ww"></script>
  </head>