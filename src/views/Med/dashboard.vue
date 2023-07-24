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
        <div style="display: flex; flex-direction: row; width: 100%; padding-left: 10%; padding-right: auto; padding-top: 7%; padding-bottom: 5%;">
            <div style="display: flex; flex-direction: column;">
                <p style="color: black; margin-top: -5%; font-size: 1.2rem; font-weight: 500; color:#3b3b3b"> Your Account</p>
                <p style="color: black; margin-top: 5%; font-size: 1.2rem;"> $7251.43</p>
            </div>
            <div class="brand-gradient" style="border-radius: .5rem; width: 3.1rem; height: 3.1rem; margin-left: 24%; margin-top: -2%;">
                <span class="material-symbols-outlined" style="margin-top: 15%; margin-left: 18%; color: #fff;">
                    view_cozy
                </span>
            </div>
        </div>
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
    // width: 18rem;
    // width: 1%;
    height: 5rem;
}

.brand-gradient {
  background: rgb(255,27,24);
  background: linear-gradient(342deg, rgba(255,27,24,1) 0%, rgba(255,149,0,1) 100%, rgba(0,212,255,1) 100%);
}
</style>
