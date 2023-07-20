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
        <h2 style="color: black; font-size: 2.5rem; margin-left: 2.5rem; margin-top: 0px;">HEALTH</h2>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 3%; top: 8%; color: black; border-radius: 1rem; width: 40%; height: 25rem; display: flex; flex-direction: column;">
        <div style="padding-left: 20%">
        <p style="color: black; font-size: 2rem;">Medications</p>
        <p style="color: black; font-size: 1.5rem; margin-top: 12rem;">Your Pharmacy: Walreds</p>
        <p style="color: black; font-size: 1.5rem;">medication 1: refill ---</p>
        <p style="color: black; font-size: 1.5rem;">medication 2: refill ---</p>
        </div>
        </div>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 47%; top: 8%; color: black; border-radius: 1rem; width: 42%; height: 25rem; display: flex; flex-direction: column;">
            <div style="padding-left: 20%">
            <p style="color: black; font-size: 2rem;">Your Doctor</p>
            <p style="color: black; font-size: 1.5rem; margin-top: 12rem;">Your Pharmacy: Walreds</p>
            <p style="color: black; font-size: 1.5rem;">medication 1: refill ---</p>
            <p style="color: black; font-size: 1.5rem;">medication 2: refill ---</p>
            </div>
        </div>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 3%; top: 53%; color: black; border-radius: 1rem; width: 86%; height: 15rem; display: flex; flex-direction: row;">
        <div style="flex:25; background:red; display:flex; flex-direction: column;">Schedule a visit</div>
        <div style="flex:25; background:blue; display:flex; flex-direction: column;">Manage medications</div>
        <div style="flex:25; background:green; display:flex; flex-direction: column;">View Health Outcomes</div>
        <div style="flex:25; background:yellow; display:flex; flex-direction: column;">Call US</div>
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
    width: 18rem;
    height: 5rem;
}
</style>
