<script>
    import { FaGgCircle, FaGratipay, FaMegaport } from 'svelte-icons/fa';
    import { navigate } from 'svelte-routing';
    import { onMount } from 'svelte';
  
    onMount(() => {
      const map = new google.maps.Map(document.getElementById('map'), {
        center: { lat: -41.27520, lng: 173.28912 }
      });
    });
  
    const userInfo = JSON.parse(localStorage.getItem('userInfo'));
  
    //guarded route to check if user is logged in if not go to login page
    const guardedRoute = () => {
      if (localStorage.getItem('userInfo') === null) {
        navigate('/Login');
      }
      if (localStorage.getItem('userInfo') !== null && userInfo.data.isMember === true) {
        navigate('/addProduct');
      }
      if (localStorage.getItem('userInfo') !== null && userInfo.data.isMember === false) {
        navigate('/Product');
      }
    };
  </script>
  
  <style>
    /* Add your styles here */
  </style>
  
  <!----------------------------- Layout Section ----------------------------->
  <head>
    <script src="https://maps.googleapis.com/maps/api/js?key=https://maps.googleapis.com/maps/api/js?key=AIzaSyDx8LN58Ol5Td4iSjtjgtTkGhqNwV8B8Ww"></script>
  </head>
  
  <div class="landing-top">
    <div class="intro-text-container">
      <h1 class="intro-text-top">Welcome to <br /> Quill Training Charity</h1>
      <button class="btn btn-primary btn-lg" id="landing-shopNow-btn" on:click={guardedRoute}>Shop Now</button>
    </div>
    <div class="landing-pic-container">
      <img class="landing-pic" alt="landing-pic" src="landing-picture.jpg" />
    </div>
  </div>
  <div class="landing-mid">
    <h1 class="intro-text-mid-title">Mission</h1>
    <div class="intro-text-container2">
      <div class="intro-text-container-left">
        <FaGgCircle class="intro-text-mid-icon" />
        <p class="intro-text-mid">Quill Training aims to provide upskilling possibilities to those in the Nelson region</p>
      </div>
      <div class="intro-text-container-right">
        <FaMegaport class="intro-text-mid-icon" />
        <p class="intro-text-mid">We aim to provide these opportunities to any and all people who wish to upskill, namely those who cannot access these resources traditionally</p>
      </div>
      <div class="intro-text-container-mid">
        <FaGratipay class="intro-text-mid-icon" />
        <p class="intro-text-mid">Our heart is to impact people in New Zealand, Allowing them to continually grow and improve.</p>
      </div>
    </div>
    <div id="map">  </div>
  </div>