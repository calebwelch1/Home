<script lang="ts">

export default {
  data() {
    return { 
      showAbout:false,
     }
  },
  mounted() { },
  methods: {
},
  };
</script>

<template>
  <main>
    <html lang="en">
<body>
  <!-- <div class="split-slideshow">
    <img class="img-one" src="https://images.pexels.com/photos/17349974/pexels-photo-17349974/free-photo-of-light-art-pattern-texture.jpeg" />
    <img class="img-two" src="https://images.pexels.com/photos/15286/pexels-photo.jpg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" />
  </div> -->
  <!-- <div class="slideshow-text">
    <div class="item" @click="$router.push('med')">Health</div>
    <div style="pointer-events: none;" class="item crossed-out-blur">Canyon</div>
    <div style="pointer-events: none;" class="item crossed-out-blur">Erosion</div>
    <div style="pointer-events: none;" class="item crossed-out-blur">Fast & Slow</div>
  </div> -->
  <div class="portfolio-container">
    <div class="portfolio-header">
      <div style="margin-left: auto; margin-right: auto; display:flex; flex-direction:column;">
        <h1 style="font-size:5.5rem; margin-bottom: 5px;">HOME</h1>
        <div style="display:flex; flex-direction: row;">
          <p style="font-size:1.1rem; margin-left:auto; margin-right: auto;">projects by
          <a style="color:white; margin:none;padding:none; height: 1rem;" href="https://calebwelch1.github.io/portfolio/">Caleb Welch</a>
          </p>
        </div>
        <!-- <div style="display:flex; flex-direction:row; justify-content:space-between;">
          <p style="cursor:pointer;">Projects</p><p>|</p><p class="crossed-out-blur">Case Studies</p>
        </div> -->
      </div>
    </div>
    <div style=" background: white; display: flex; flex-direction: column; height: 78vh;">
      <div style="display: flex; flex-direction: row; justify-content: space-between; gap: 5vw; margin-top: 2%; margin-bottom: 2%; width: 90%; margin-left: auto; margin-right: auto; font-size: 1.3rem;">
        <div style="flex:40; position:relative;">
        <div class="diagonal-square" style="position:absolute; flex: 40; height: 100%; width: 100%;"/>
        <img src="./myhealth.png" class="drop-shadow-xl" style="z-index: 5; hight: 50%; width: 80%; position: absolute; bottom: -5%; right: -3%;"/>
        </div>
        <!-- <div class="diagonal-square" style="flex:40;"></div> -->
        <div style="display: flex; flex-direction: column; justify-content: space-between; flex: 60;">
          <h3 style="font-size: 2rem;">MyHealth+</h3>
        <p style="font-size:1.5rem; margin-bottom: 2%;">MyHealth+ is an ambitious and innovative project that sets out to revolutionize the user interface and user experience for patients within the realm of online healthcare portals. In today's fast-paced digital world, easy access to healthcare information and seamless patient interactions are paramount. With this vision in mind, MyHealth+ emerges as a transformative solution, aiming to create a dynamic and intuitive platform that bridges the gap between patients and their medical journey. At its core, MyHealth+ prioritizes user-centric design, elevating the way patients interact with their healthcare data and providers. By combining cutting-edge UI/UX principles, the project seeks to craft an engaging and personalized experience for every individual, fostering a sense of empowerment and involvement in their own healthcare decisions. Whether it's viewing medical records, booking appointments, or securely communicating with healthcare professionals, MyHealth+ brings efficiency and transparency to the forefront.</p>
        <button class="portfolio-button" @click="$router.push('med')">Visit</button>
        </div>
      </div>
    </div>
  </div>
</body>
</html>
  </main>
</template>
<style lang="scss">
body,
html {
  height: 100%;
  background: #110101;
  overflow: hidden;
}

.portfolio-container {
  height:100%; width: 100%; border: 1px solid red; display: flex; flex-direction: column; overflow: hidden;
}

.portfolio-header {
  background: black; color:white; display: flex; flex-direction:row; height: 22vh;
}

.split-slideshow {
  position: relative;
}
.img-one {
        min-width: 101%;
        min-height: 101%;
        position: absolute;
        top: 100%;
        left: 50%;
        transform: translate(-100%, -0%);
        z-index: 2;
      }

.img-two {
        min-width: 101%;
        min-height: 101%;
        position: absolute;
        top: 100%;
        right: 50%;
        transform: translate(100%, 0%);
      }

.slideshow-text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 100;
  font-size: 80px;
  width: 100vw;
  text-align: center;
  color: #fff;
  font-family: 'Roboto Condensed', sans-serif;
  font-weight: 100;
  text-transform: uppercase;
  letter-spacing: 20px;
  line-height: 0.8;
  
  @media (max-width: 767px) {
    font-size: 40px;
  }
  
}

.item {
  cursor: pointer;
  margin-bottom: 1rem;
}

.the-most {
  position: fixed;
  z-index: 1;
  bottom: 0;
  left: 0;
  width: 50vw;
  max-width: 200px;
  padding: 10px;
  
  img {
    max-width: 100%;
  }
}

.crossed-out-blur {
  /* Add a text-decoration line to cross out the word */
  text-decoration: line-through;

  /* Add a white text-shadow to simulate a blur effect */
  text-shadow: 0 0 5px white;
}

.background-gradient {
  background: rgb(230,178,57);
  background: linear-gradient(135deg, rgba(230,178,57,1) 0%, rgba(215,12,12,1) 100%, rgba(210,41,41,1) 100%);
}

.diagonal-square {
    position: relative;
    width: 100%;
    height: 100%;
    background: rgb(230,178,57);
    background: linear-gradient(135deg, rgba(230,178,57,1) 0%, rgba(215,12,12,1) 100%, rgba(210,41,41,1) 100%);
    clip-path: polygon(0 0%, 100% 0, 0 100%, 0 100%);
}

.diagonal-square::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 20%;
    background: rgb(230,178,57);
    background: linear-gradient(135deg, rgba(230,178,57,1) 0%, rgba(215,12,12,1) 100%, rgba(210,41,41,1) 100%); /* You can set the same background color as the square */
    clip-path: polygon(0 0%, 100% 0, 0 100%, 0 100%);
}

.drop-shadow-xl {
    filter: drop-shadow(0 20px 13px rgb(0 0 0 / 0.03)) drop-shadow(0 8px 5px rgb(0 0 0 / 0.08));
}

.portfolio-button {
  height: 4rem;
  width: 23rem;
  background: black;
  color: white;
  border-radius: 10rem;
  font-size: 1.5rem;
  margin-left: auto;
  margin-right: auto;
  font-weight:600;
  letter-spacing:0.2em;
  border:none;
  cursor:pointer;
  transition: background-color 0.2s, transform 0.1s;
}

.portfolio-button:hover {
  background-color: #333; /* Slightly darker color on hover */
}

.portfolio-button:active {
  background-color: #222; /* Even darker color on button press */
  transform: translateY(2px); /* Slight vertical shift to simulate button press */
}
</style>

