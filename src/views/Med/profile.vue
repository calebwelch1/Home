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
    <div class="dashboard">
        <h2 style="color: black; font-size: 2.5rem; margin-left: 2.5rem; margin-top: 0px;">Profile</h2>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 4%; top: 7%; color: black; border-radius: 1rem; width: 100%; max-width: 200px; height: 45rem;
        display: flex; flex-direction: column; justify-content: center; padding: 0% 10%;">
        <span class="material-symbols-outlined" style="color: #545454;">
                person
        </span>
            
        </div>
    </div>
</template>
<style lang="scss">

.material-symbols-outlined {
        font-variation-settings:
        'FILL' 0,
        'wght' 400,
        'GRAD' 0,
        'opsz' 48;
        font-size: 2rem !important;
}

body,
html {
  height: 100%;
  background: #110101;
  font-family: 'Roboto', sans-serif;
  overflow: hidden;
}

.dashboard {
    background: #f2f2f2;
    width: 100%;
    height: 100%;
    position: relative;
}

.container {
  display: flex;
  height: 100%;
  width: 100%;
  padding: 0px;
}

.absolute {
    position: absolute;
}
.first-div {
  flex: 20;
  background-color: #f0f0f0;
}

.second-div {
  flex: 80;
  background-color: #d0d0d0;
}

.main {
    min-height: 100vh;
    min-width: 79vw;
    max-width: 79vw;
    background: forestgreen;
}

.tag-card {
    background: #fff;
    color: black;
    border-radius: 1rem;
    width: 18rem;
    height: 5rem;
}
</style>
