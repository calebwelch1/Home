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
    <div class="item" @click="$router.push('med')">Canyon</div>
    <div class="item" @click="$router.push('Shop')">Desert</div>
    <div class="item" @click="$router.push('Shop')">Erosion</div>
    <div class="item" @click="$router.push('Shop')">Shape</div>
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
  cursor: pointer;
  
  @media (max-width: 767px) {
    font-size: 40px;
  }
  
}

.item {
  cursor: pointer;
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
</style>

