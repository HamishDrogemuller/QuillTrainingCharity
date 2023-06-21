<script>
      import { FaGgCircle, FaGratipay, FaMegaport } from 'svelte-icons/fa';
      import '../landing.css';
</script>

<!----------------------------- Layout Section -----------------------------> 
<div class="landing-top">
  <div class="intro-text-container">
    <h1 class="intro-text-top">Welcome to <br /> Quill Training Charity</h1>
  </div>
  <div class="landing-pic-container">
    <img class="landing-pic" alt="landing-pic" src= "../../public/landing-picture.jpg"/>
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
</div>