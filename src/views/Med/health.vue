<script lang="ts">
import doctor from './healthcare-provider-portrait.jpg';

export default {
  data() {
    return { 
      showAbout:false,
      doctor,
     }
  },
  mounted() { },
  methods: {
},
  };
</script>

<template>
    <div class="dashboard">
        <!-- <h2 style="color: black; font-size: 2.5rem; margin-left: 2.5rem; margin-top: 0px;">HEALTH</h2> -->
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 3%; top: 8%; color: black; border-radius: 1rem; width: 40%; height: 25rem; display: flex; flex-direction: column;">
        <div style="padding-left: 20%">
        <p style="color: black; font-size: 2rem; margin-bottom: 18%; ">Medications</p>
        <p style="color: black; font-size: 1.5rem;">Your Pharmacy: Walreds</p>
        <p style="color: black; font-size: 1.5rem;">medication 1: refill ---</p>
        <p style="color: black; font-size: 1.5rem;">medication 2: refill ---</p>
        </div>
        </div>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 47%; top: 8%; color: black; border-radius: 1rem; width: 42%; height: 25rem; display: flex; flex-direction: column; align-items: center; justify-content: center;">
            <div style="padding-left: 5%">
            <p style="color: black; font-size: 2rem; margin-bottom: 18%; ">Your Doctor</p>
            <img :src="doctor" style="height: 100%; width: 100%; max-height: 150px; max-width: 200px;"/>
            <p style="color: black; font-size: 1.5rem;"></p>
            <p style="color: black; font-size: 1.5rem;">Dr. Kalimisetty</p>
            <p style="color: black; font-size: 1.5rem;">Make an appointment</p>
            </div>
        </div>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 3%; top: 53%; color: black; border-radius: 1rem; width: 86%; height: 15rem; display: flex; flex-direction: row;">
        <div style="flex:25; background:white; display:flex; flex-direction: column;  align-items: center; justify-content: center; border-radius: 1rem 0rem 0rem 1rem;">
          <span class="material-symbols-outlined" style="font-size: 8rem !important; color: grey; margin-left: 0%; margin-top: 2%;">
            calendar_month
          </span>
        <p style="margin-left: 0%; font-size: 1.5rem; font-weight: 500; ">
          Schedule a visit
        </p> 
        </div>
        <div style="flex:25; background:grey; display:flex; flex-direction: column;  align-items: center; justify-content: center;">
          <span class="material-symbols-outlined" style="font-size: 8rem !important; color: white; margin-left: 0%; margin-top: 2%;">
            pill
          </span>
        <p style="margin-left: 0%; font-size: 1.5rem; font-weight: 500; color: white;">
          Manage medications
        </p> 
        </div>
        <div style="flex:25; background:white; display:flex; flex-direction: column;  align-items: center; justify-content: center;">
          <span class="material-symbols-outlined" style="font-size: 8rem !important; color: grey; margin-left: 0%; margin-top: 2%;">
            monitor_heart
          </span>
        <p style="margin-left: 0%; font-size: 1.5rem; font-weight: 500; ">
          View Health Outcomes
        </p>  
        </div>
        <div style="flex:25; background:grey; display:flex; flex-direction: column;  align-items: center; justify-content: center;border-radius: 0rem 1rem 1rem 0rem;" >
          <span class="material-symbols-outlined" style="font-size: 8rem !important; color: white; margin-left: 0%; margin-top: 2%;">
            phone_in_talk
          </span>
        <p style="margin-left: 0%; font-size: 1.5rem; font-weight: 500; color: white;">
          Call US
        </p>
        </div>
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

.material-symbols-outlined {
        font-variation-settings:
        'FILL' 0,
        'wght' 400,
        'GRAD' 0,
        'opsz' 48;
        font-size: 2rem !important;
}
</style>
