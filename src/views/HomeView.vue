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
  <div class="split-slideshow">
    <img class="img-one" src="https://images.pexels.com/photos/17349974/pexels-photo-17349974/free-photo-of-light-art-pattern-texture.jpeg" />
    <img class="img-two" src="https://images.pexels.com/photos/15286/pexels-photo.jpg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" />
  <!-- <div class="slideshow">
    <div class="slider">
      <div class="item">
        <img class="img-one" src="https://images.pexels.com/photos/17349974/pexels-photo-17349974/free-photo-of-light-art-pattern-texture.jpeg" />
        <img class="img-two" src="https://images.pexels.com/photos/15286/pexels-photo.jpg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" />
      </div>
    </div> -->
  </div>
  <div class="slideshow-text">
    <div class="item" @click="$router.push('med')">Health</div>
    <div style="pointer-events: none;" class="item crossed-out-blur">Canyon</div>
    <div style="pointer-events: none;" class="item crossed-out-blur">Erosion</div>
    <div style="pointer-events: none;" class="item crossed-out-blur">Fast & Slow</div>
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
  font-family: 'Roboto', sans-serif;
  overflow: hidden;
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
</style>

