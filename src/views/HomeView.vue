<script lang="ts">

export default {
  data() {
    return { 
      showAbout:false,
      windowWidth: window.innerWidth,
     }
  },
  mounted() {
    this.$nextTick(() => {
      window.addEventListener('resize', this.onResize);
    })
  },
  beforeDestroy() { 
    window.removeEventListener('resize', this.onResize); 
  },
  methods: {  
    onResize() {
      this.windowWidth = window.innerWidth
    },
    routeCC() {
      window.open('https://calebwelch1.github.io/c-collection'); 
    },
    routePortfolio() {
      window.open('https://calebwelch1.github.io/art'); 
    },
    routeLittleLemon() {
      window.open('https://github.com/calebwelch1/little-lemon-react-native'); 
    },
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
    <div style=" background: white; display: flex; flex-direction: column; height: 78vh; overflow-y: scroll; overflow-x:hidden;">
      <div class="project-container" style="">
        <div v-if="windowWidth > 1360" class="project-image-container" style="">
        <div class="diagonal-square-brown project-gradient-square-size"/>
        <img src="./art_portfolio.png" class="drop-shadow-xl project-image-position" style=""/>
        </div>
        <div v-else>
          
          <img src="./art_portfolio.png" class="drop-shadow-xl project-image-position" style=""/>
        </div>
        <div class="project-text-container" style="">
          <h3 style="font-size: 2rem;">Art Portfolio</h3>
        <p style="font-size:1.5rem; margin-bottom: 2%; margin-top: 8rem; margin-bottom:8rem;">A personal website  I built to host my art.</p>
        <button class="portfolio-button" @click="routePortfolio">Visit</button>
        </div>
      </div>
      <div class="project-container" style="">
        <div v-if="windowWidth > 1360" class="project-image-container" style="">
        <div class="diagonal-square-yellow project-gradient-square-size"/>
        <img src="./littleLemon.png" class="drop-shadow-xl project-image-position" style=""/>
        </div>
        <div v-else>
          <!-- <img src="./myhealth.png" class="drop-shadow-xl" style="height:60vh; width:75vw;"/> -->
          <img src="./littleLemon.png" class="drop-shadow-xl project-image-position" style=""/>
        </div>
        <!-- <div class="diagonal-square" style="flex:40;"></div> -->
        <div class="project-text-container" style="">
          <h3 style="font-size: 2rem;">Little Lemon React Native</h3>
        <p style="font-size:1.5rem; margin-bottom: 2%;">Little Lemon is a React Native project for the fictional Chicago Restuarant of the same name. This project showcases my abilities to create cross platform mobile applications ( Android and iOS ) from start to finish. From Figma wireframes to authentication and login, rendering restuarant items with asynchronous calls and storing application information in databases sucha s AsyncStorage and SQLite - Little Lemon is a comprehensive application and a testament to my continuous growth in software.</p>
        <button class="portfolio-button" @click="routeLittleLemon">Visit</button>
        </div>
      </div>
      <div class="project-container" style="">
        <div v-if="windowWidth > 1360" class="project-image-container" style="">
        <div class="diagonal-square project-gradient-square-size"/>
        <img src="./myhealth.png" class="drop-shadow-xl project-image-position" style=""/>
        </div>
        <div v-else>
          <img src="./myhealth.png" class="drop-shadow-xl" style="height:60vh; width:75vw;"/>
        </div>
        <!-- <div class="diagonal-square" style="flex:40;"></div> -->
        <div class="project-text-container" style="">
          <h3 style="font-size: 2rem;">MyHealth+</h3>
        <p style="font-size:1.5rem; margin-bottom: 2%;">MyHealth+ is an ambitious and innovative project that sets out to revolutionize the user interface and user experience for patients within the realm of online healthcare portals. In today's fast-paced digital world, easy access to healthcare information and seamless patient interactions are paramount. With this vision in mind, MyHealth+ emerges as a transformative solution, aiming to create a dynamic and intuitive platform that bridges the gap between patients and their medical journey. At its core, MyHealth+ prioritizes user-centric design, elevating the way patients interact with their healthcare data and providers. By combining cutting-edge UI/UX principles, the project seeks to craft an engaging and personalized experience for every individual, fostering a sense of empowerment and involvement in their own healthcare decisions. Whether it's viewing medical records, booking appointments, or securely communicating with healthcare professionals, MyHealth+ brings efficiency and transparency to the forefront.</p>
        <button class="portfolio-button" @click="$router.push('med')">Visit</button>
        </div>
      </div>
      <div class="project-container" style="">
        <div v-if="windowWidth > 1360" class="project-image-container" style="">
        <div class="diagonal-square-blue project-gradient-square-size"/>
        <img src="./ccollection.png" class="drop-shadow-xl project-image-position" style=""/>
        </div>
        <div v-else>
          <img src="./ccollection.png" class="drop-shadow-xl" style="height:60vh; width:75vw;"/>
        </div>
        <!-- <div class="diagonal-square" style="flex:40;"></div> -->
        <div class="project-text-container" style="">
          <h3 style="font-size: 2rem;">C-Collection</h3>
        <p style="font-size:1.5rem; margin-bottom: 2%;">C-collection captivating portfolio project, serving as a delightful homage to the profound impact of media on one's journey of self-discovery. Inspired by the timeless elegance of the Criterion Collection website, this meticulously crafted project offers a unique perspective into the diverse world of books, movies, and other cherished media that have shaped and influenced personal growth. With a keen eye for modern UI aesthetics, the project seamlessly weaves together an artful tapestry of film covers, book artworks, and captivating synopses, providing visitors with an immersive and aesthetically pleasing experience. Journey through an eclectic selection of works that have profoundly resonated with the creator.</p>
        <button class="portfolio-button" @click="routeCC">Visit</button>
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
  height:100%; width: 100%; display: flex; flex-direction: column; overflow:hidden;
}

.portfolio-header {
  background: black; color:white; display: flex; flex-direction:row; height: 22vh;
}

.project-container {
  display: flex; flex-direction: row; justify-content: space-between; gap: 5vw; margin-top: 2%; margin-bottom: 2%; width: 90%; margin-left: auto; margin-right: auto; font-size: 1.3rem; height: 60vh;
}

.project-image-position {
  z-index: 5; height: 75%; width: 80%; position: absolute; bottom: -5%; right: -3%;
}

.project-gradient-square-size {
  position:absolute; flex: 40; height: 100%; width: 100%;
}

.project-image-container {
  flex:40; position:relative; height: 90%; width: 100%;
}

.project-text-container {
  display: flex; flex-direction: column; justify-content: space-between; flex: 60;
}

@media (max-width: 1360px) {
  .project-container {
  display: flex; flex-direction: column; justify-content: space-between; gap: 5vw; margin-top: 2%; margin-bottom: 2%; width: 80%; margin-left: auto; margin-right: auto; font-size: 1.3rem; height: 100rem;
}

.project-image-container {
  position:relative; border: 1px solid red; height: 90rem; width: 100%; display:block;
}

.project-text-container {
  display: flex; flex-direction: column; justify-content: space-between;
}

.project-image-position {
  z-index: 5; height: 90%; width: 80%; position: absolute; bottom: -5%; right: -3%;
}
  }
.split-slideshow {
  position: relative;
}
// under 1260
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

.diagonal-square-blue {
  position: relative;
    width: 100%;
    height: 100%;
    clip-path: polygon(0 0%, 100% 0, 0 100%, 0 100%);
  background: rgb(77,203,221);
background: linear-gradient(135deg, rgba(77,203,221,1) 0%, rgba(12,40,215,1) 100%, rgba(210,41,41,1) 100%);
}

.diagonal-square-blue::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 20%;
    background: rgb(77,203,221);
background: linear-gradient(135deg, rgba(77,203,221,1) 0%, rgba(12,40,215,1) 100%, rgba(210,41,41,1) 100%);
    clip-path: polygon(0 0%, 100% 0, 0 100%, 0 100%);
}

.diagonal-square-yellow {
  position: relative;
    width: 100%;
    height: 100%;
    clip-path: polygon(0 0%, 100% 0, 0 100%, 0 100%);
    background: #CFBE53;
background: linear-gradient(to right, #CFBE53 0%, #CFFF30 30%, #A4FF54 60%, #82CF97 100%);
}

.diagonal-square-yellow::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 20%;
    background: #CFBE53;
background: linear-gradient(to right, #CFBE53 0%, #CFFF30 30%, #A4FF54 60%, #82CF97 100%);
    clip-path: polygon(0 0%, 100% 0, 0 100%, 0 100%);
}

.diagonal-square-brown {
  position: relative;
    width: 100%;
    height: 100%;
    clip-path: polygon(0 0%, 100% 0, 0 100%, 0 100%);
   background: rgb(36,0,0);
   background: linear-gradient(90deg, rgba(36,0,0,1) 0%, rgba(148,119,31,1) 100%, rgba(0,212,255,1) 100%);

}

.diagonal-square-brown::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 20%;
   background: rgb(36,0,0);
   background: linear-gradient(90deg, rgba(36,0,0,1) 0%, rgba(148,119,31,1) 100%, rgba(0,212,255,1) 100%);
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

