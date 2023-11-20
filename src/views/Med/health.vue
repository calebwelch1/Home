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
        <!-- <div class="modal drop-shadow-xl"
        style="top: 2%; left: 2%; height: 100%; width: 100%; max-height: 77vh; max-width:75vw; background: grey; border-radius: 2rem; position: absolute; z-index: 99;"
        >
        <div style="display:flex; height: 90%; width: 90%; margin-left: 5%; margin-top: 2.5%; gap: 2%;">

        </div> -->
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 3%; top: 8%; color: black; border-radius: 1rem; width: 40%; height: 25rem; display: flex; flex-direction: column;align-items: center; justify-content: center; padding-left: 1rem;">
          <div style="display: flex; flex-direction: row; width: 100%; justify-content: center; gap: 2rem;margin-left: auto; margin-right: auto;padding-top: 2rem;">
              <div style="margin-top:auto; margin-bottom: auto;" class="cursor">
                <span class="material-symbols-outlined" style="font-size: 2rem !important; color: red; margin-left: 0%; margin-top: 2%;">
                  phone_in_talk
                </span>
                <p style="color:red">call</p>
              </div>
              <div>
                <p style="color: black; font-size: 2rem; margin-bottom: 4%; margin-top: -3rem; margin-right: -1rem; text-align: center;">Your Pharmacy</p>
                <span class="material-symbols-outlined" style="font-size: 8rem !important; color: red; margin-left: 22%; margin-right: auto; margin-top: 2%; text-align: center;">
                local_pharmacy
                </span>
                <p style="color: black; font-size: 1.5rem;"></p>
                <p style="color: black; font-size: 1.5rem; text-align:center; margin-top: 1rem;">Walreds</p>
              </div>
              <div style="margin-top:auto; margin-bottom: auto; display: flex; flex-direction: column;" class="cursor">
                <span class="material-symbols-outlined" style="font-size: 2rem !important; color: red; margin-left: auto; margin-right: auto; margin-top: 2%;">
                  pill
                </span>
                <p style="color:red">medications</p>
              </div>
            </div>
        </div>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 47%; top: 8%; color: black; border-radius: 1rem; width: 41%; height: 25rem; display: flex; flex-direction: column; align-items: center; justify-content: center; padding-left: 1rem;">
            <div style="display: flex; flex-direction: row; width: 100%; justify-content: center; gap: 2rem;margin-left: auto; margin-right: auto;">
              <div style="margin-top:auto; margin-bottom: auto;" class="cursor">
                <span class="material-symbols-outlined" style="font-size: 2rem !important; color: red; margin-left: 0%; margin-top: 2%;">
                  phone_in_talk
                </span>
                <p style="color:red">call</p>
              </div>
              <div>
                <p style="color: black; font-size: 2rem; margin-bottom: 4%; margin-top: -3rem; text-align: center;">Your Doctor</p>
                <img :src="doctor" class="round-avatar" style="height: 100%; width: 100%; max-height: 200px; max-width: 200px; border: 2px solid grey;"/>
                <p style="color: black; font-size: 1.5rem;"></p>
                <p style="color: black; font-size: 1.5rem; text-align:center; margin-top: 1rem;">Dr. Ramani</p>
              </div>
              <div style="margin-top:auto; margin-bottom: auto; display: flex; flex-direction: column;" class="cursor">
                <span class="material-symbols-outlined" style="font-size: 2rem !important; color: red; margin-left: auto; margin-right: auto; margin-top: 2%;">
                  calendar_month
                </span>
                <p style="color:red">schedule</p>
              </div>
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

.round-avatar {
  border-radius: 50%; /* Make the element round */
  object-fit: cover; /* Preserve aspect ratio and cover the entire element */
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
