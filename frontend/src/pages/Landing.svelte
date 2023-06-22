<script>
      import { FaGgCircle, FaGratipay, FaMegaport } from 'svelte-icons/fa';
      import Map from './map.svelte';
      
</script>

<!----------------------------- Layout Section -----------------------------> 
<div class="landing-top" style="background-image: url('../../public/landing-picture.jpg');background-size: cover;background-position: center;">
  <div class="intro-text-container">
    <h1 class="intro-text-top">Welcome to Quill Training Charity</h1>
  </div>
  <div class="landing-pic-container">
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
  <div class="map-container">
    <Map />
  </div>
</div>

<style>
  

.landing-top {
	display: grid;
	grid-template-columns: 1fr 1fr;
	gap: 10px;
	background-color: goldenrod;
	color: #fff;
	height: 30vh;
	align-items: center;
	
  }
  
  .intro-text-container {
	width: 30rem;
  }
  
  .intro-text-top {
	font-size: 4rem;
	text-align: center;
	margin: 0;
  }
  
  .landing-pic-container {
	background-image: url("../public/landing-picture.png");
	width: 300px;
	height: 300px;
	border-radius: 50%;
	overflow: hidden;
  }
  
  .landing-pic {
	width: 100%;
	height: auto;
	
  }
  
  .landing-mid {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	background-color: #eee;
	height: 40vh;
	margin-bottom: 5rem;
  }
  
  .intro-text-mid-title {
	font-size: 2rem;
	text-align: center;
	margin: 0;
  }
  
  .intro-text-container2 {
	display: grid;
	grid-template-columns: repeat(3, 1fr);
	gap: 10px;
	margin-top: 2rem;
  }
  
  .intro-text-container-left, .intro-text-container-right, .intro-text-container-mid {
	display: flex;
	flex-direction: column;
	align-items: center;
	text-align: center;
  }
  
  .intro-text-mid-icon {
	font-size: 30px;
	margin-bottom: 1.5rem;
  }
  
  .intro-text-mid {
	font-size: 1rem;
	margin: 0;
  }
/* Styles for screens larger than 768px */
@media only screen and (min-width: 768px) {
	.landing-top {
	  height: 50vh;
	}
  
	.intro-text-container {
	  width: 40rem;
	}
  
	.landing-pic-container {
	  width: 400px;
	  height: 400px;
	}
  
	.landing-mid {
	  height: 60vh;
	}
  }
  
  /* Styles for screens larger than 1024px */
  @media only screen and (min-width: 1024px) {
	.landing-top {
	  height: 60vh;
	}
  
	.intro-text-container {
	  width: 50rem;
	}
  
	.landing-pic-container {
	  width: 500px;
	  height: 500px;
	}
  
	.landing-mid {
	  height: 70vh;
	}
  }
</style>