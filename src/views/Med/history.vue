<script lang="ts">
import healthBanner from './healthBanner.png'
export default {
  data() {
    return { 
      showAbout:false,
      healthBanner,
     }
  },
  mounted() { },
  methods: {
},
  };
  // links to news stories
  // https://hospitalnews.com/pharmacogenomic-testing-promising-treatment-for-depression/
  // https://hospitalnews.com/enhancing-the-patient-experience-with-essential-care-partner-programs/
  // https://hospitalnews.com/treating-high-risk-drinking-alcohol-use-disorder-new-canadian-guideline/
</script>

<template>
   <div class="dashboard">
        <img :src="healthBanner" style="max-height: 12rem; max-width: 100%; height: 100%; width: 100%; object-fit: cover;" />
        <div style="display: flex; flex-direction: row; justify-content: space-between; height: 100%; width: 100%; max-width:100%; max-height:18rem; border: 1px solid red;">
          <p style="color: black;">image</p>
          <p style="color: black;">story</p>
          <p style="color: black;">image</p>
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
    overflow-y: scroll;
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
