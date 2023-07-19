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
    <div style="height: 100vw; width: 100vw; overflow: hidden;">
        <div class="sidebar">hi</div>
        <div class="main">hello</div>
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
  overflow: scroll;
}

.sidebar {
        min-width: 20vw;
        max-width: 20vw;
        width: 20vw;
        min-height: 100vh;
        background-color: blueviolet;
        margin-right: 0px;
      }

.main {
    min-height: 100vh;
    min-width: 79vw;
    max-width: 79vw;
    background: forestgreen;
}
</style>
