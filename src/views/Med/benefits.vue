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
        <h2 style="color: black; font-size: 2.5rem; margin-left: 2.5rem; margin-top: 0px;">Your Health Statistics</h2>
        <div
        class="drop-shadow-xl absolute tag-card"
        style="left: 3%; top: 10%; width: 18%;">
        1
        </div>
        <div
        class="drop-shadow-xl absolute tag-card"
        style="left: 24%; top: 10%; width: 18%;">
        2
        </div>
        <div
        class="drop-shadow-xl absolute tag-card"
        style="left: 3%; top: 21%; width: 18%;">
        3
        </div>
        <div
        class="drop-shadow-xl absolute tag-card"
        style="left: 24%; top: 21%; width: 18%;">
        4
        </div>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 3%; top: 36%; color: black; border-radius: 1rem; width: 39%; height: 16rem;">
            big
        </div>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 50%; top: 10%; color: black; border-radius: 1rem; width: 39%; height: 50%;">
            big 2
        </div>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 20%; top: 66%; color: black; border-radius: 1rem; width: 54%; height: 10rem;">
            footer
        </div>
    </div>
</template>
<style lang="scss">
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
    height: 5rem;
}
</style>
