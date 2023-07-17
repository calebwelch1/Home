<script lang="ts">


export default {
  data() {
    return { 
      showAbout:false,
     }
  },
  mounted() {
  },
  methods: {
},
  };
</script>

<template>
  <main>
    <html lang="en">
<body>
    <p style="color: white; font-size: 40rem;"> HOME!</p>
</body>
</html>
  </main>
</template>
<style>
.about-enter-active {
  transition: all 0.5s ease-out;
}

.about-leave-active {
  transition: all 0.5s ease-out;
}

.about-enter-from,
.about-leave-to {
  transform: translateX(-200px);
  opacity: 0;
}

.work-enter-active {
  transition: all 0.5s ease-out;
}

.work-leave-active {
  transition: all 0.5s ease-out;
}

.work-enter-from,
.work-leave-to {
  transform: translateX(200px);
  opacity: 0;
}


.contact-enter-active {
  transition: all 0.5s ease-out;
}

.contact-leave-active {
  transition: all 0.5s ease-out;
}

.contact-enter-from,
.contact-leave-to {
  transform: translateY(200px);
  opacity: 0;
}

.filter-white{
  filter: invert(100%) sepia(4%) saturate(7482%) hue-rotate(233deg) brightness(113%) contrast(95%);
}

.h-2 {
  height:2rem;
}

.w-2 {
  width: 2rem;
}
</style>

