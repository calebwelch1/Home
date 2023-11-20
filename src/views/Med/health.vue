<script lang="ts">
import doctor from './healthcare-provider-portrait.jpg';
import walreds from '../../assets/walreds.png'
export default {
  data() {
    return { 
      showAbout:false,
      doctor,
      walreds,
     }
  },
  mounted() { },
  methods: {
    medOnClick(){
      const modal = document.getElementById("medModal");
      modal!.style.display = "block";
    },
    spanOnClick(){
    const modal = document.getElementById("medModal");
    modal!.style.display = "none";
    },
    scheduleOnClick(){
      const schedule = document.getElementById("scheduler")
      schedule!.style.display = "block";
    },
    onChangeDatePicker(){
      console.log('onchange')
      const schedule = document.getElementById("scheduler")
      schedule!.style.display = "none";
      const calendarNotification = document.getElementById("calendarNotification");
      calendarNotification!.style.display = "flex";
      setTimeout(() => {
        calendarNotification!.style.display = "none";
      }, 3000)
    }
},
  };
</script>

<template>
    <div class="dashboard">
        <h2 style="color: black; font-size: 2.5rem; margin-left: 2.5rem; margin-top: 0px;">HEALTH</h2>
        <div id="calendarNotification" class="modal drop-shadow-xl"
        style="top: 2%; right: 2%; height: 100%; width: 100%; max-height: 7vh; max-width:15vw; background: white; border-radius: 2rem; position: absolute; z-index: 50;flex-direction: column; justify-content: center; border: 2px solid red;"
        >
        <p style="font-size:20px; margin: auto; color: red">Appointment Set!</p>
        </div>
        <div id="medModal" class="modal drop-shadow-xl"
        style="top: 2%; left: 2%; height: 100%; width: 100%; max-height: 77vh; max-width:75vw; background: grey; border-radius: 2rem; position: absolute; z-index: 99;"
        >
        <!-- modal container -->
          <div style="display:flex; height: 85%; width: 90%; margin-left: 5%; margin-top: 5%; margin-bottom: 5%; gap: 2%; position: relative;">
        <span style="height: 9rem; width: 9rem; font-Size: 9rem; z-index: 101; position: absolute; top: -15%; right: -7%; cursor: pointer;" @click="spanOnClick">&times;</span>
        <!-- left -->
            <div style="flex: 30; background: none; width: 100%; height: 100%; display: flex; flex-direction: column; justify-content: flex-start; gap: 0;">
              <img :src="walreds" style="height: 100%; width: 100%; max-height: 450px; max-width: 350px; border-radius: 2rem;"/>
              <div class="message-box" style="margin-top: 2rem;">
                <div class="icon-text-row">                
                  <span class="material-symbols-outlined" style="margin-right:0.5rem;margin-top:-0.2rem;">
                    location_on
                  </span>
                <p class="message-header">555 Pharmacy Way, Medtown New York, New York</p>
                </div>
              </div>
              <div class="message-box">
                <div class="icon-text-row">                
                  <span class="material-symbols-outlined" style="margin-right:0.5rem;margin-top:-0.2rem;">
                    phone_in_talk
                  </span>
                  <p class="message-header">Phone: 555-555-5555</p>
              </div>
              </div>
            </div>
            <!-- right -->
            <div style="flex: 70; background: #7d7d7d;; width: 100%; height: 100%;  display: flex; flex-direction: column; justify-content: flex-start;">
              <p style="color: white; font-size: 25px;">Medications</p>
              <div style="margin-left: auto; margin-right:auto; width: 100%; border: 1px solid white; height: 90%;">
                <div style="height:2rem; border: 1px solid white; width: 100%; display: flex; flex-direction:row; justify-content: space-between;">
                  <p>
                    Medication 1
                  </p>
                  <p>
                    Dr. Ramani
                  </p>
                  <p>
                    Refill Due: 10/10/20XX
                  </p>
                </div>
                <div style="height:2rem; border: 1px solid white; width: 100%; display: flex; flex-direction:row; justify-content: space-between;">
                  <p>
                    Medication 2
                  </p>
                  <p>
                    Dr. Ramani
                  </p>
                  <p>
                    Refill Due: 10/10/20XX
                  </p>
                </div>
                <div style="height:2rem; border: 1px solid white; width: 100%; display: flex; flex-direction:row; justify-content: space-between;">
                  <p>
                    Medication 3
                  </p>
                  <p>
                    Dr. Ramani
                  </p>
                  <p>
                    Refill Due: 10/10/20XX
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 3%; top: 8%; color: black; border-radius: 1rem; width: 40%; height: 25rem; display: flex; flex-direction: column;align-items: center; justify-content: center; padding-left: 1rem;">
          <div style="display: flex; flex-direction: row; width: 100%; justify-content: center; gap: 2rem;margin-left: auto; margin-right: auto;padding-top: 2rem;">
              <div style="margin-top:auto; margin-bottom: auto;" class="cursor" @click="medOnClick">
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
              <div style="margin-top:auto; margin-bottom: auto; display: flex; flex-direction: column;" class="cursor" @click="medOnClick">
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
              <div style="margin-top:auto; margin-bottom: auto;" class="cursor" @click="medOnClick">
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
              <div style="margin-top:auto; margin-bottom: auto; display: flex; flex-direction: column;" class="cursor" @click="scheduleOnClick">
                <span class="material-symbols-outlined" style="font-size: 2rem !important; color: red; margin-left: auto; margin-right: auto; margin-top: 2%;">
                  calendar_month
                </span>
                <p style="color:red">schedule</p>
                <input type="date" id="scheduler" name="trip-start" min="2023-12-01" max="2024-12-31" :onChange="onChangeDatePicker" />
              </div>
            </div>
        </div>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 3%; top: 53%; color: black; border-radius: 1rem; width: 86%; height: 15rem; display: flex; flex-direction: row;">
        <div class="cursor" @click="scheduleOnClick" style="flex:25; background:white; display:flex; flex-direction: column;  align-items: center; justify-content: center; border-radius: 1rem 0rem 0rem 1rem;">
          <span class="material-symbols-outlined" style="font-size: 8rem !important; color: grey; margin-left: 0%; margin-top: 2%;">
            calendar_month
          </span>
        <p style="margin-left: 0%; font-size: 1.5rem; font-weight: 500; ">
          Schedule a visit
        </p> 
        </div>
        <div class="cursor" @click="medOnClick" style="flex:25; background:grey; display:flex; flex-direction: column;  align-items: center; justify-content: center;">
          <span class="material-symbols-outlined" style="font-size: 8rem !important; color: white; margin-left: 0%; margin-top: 2%;">
            pill
          </span>
        <p style="margin-left: 0%; font-size: 1.5rem; font-weight: 500; color: white;">
          Manage medications
        </p> 
        </div>
        <div class="cursor" style="flex:25; background:white; display:flex; flex-direction: column;  align-items: center; justify-content: center;">
          <span class="material-symbols-outlined" style="font-size: 8rem !important; color: grey; margin-left: 0%; margin-top: 2%;">
            monitor_heart
          </span>
        <p style="margin-left: 0%; font-size: 1.5rem; font-weight: 500; ">
          View Health Outcomes
        </p>  
        </div>
        <div class="cursor" @click="medOnClick" style="flex:25; background:grey; display:flex; flex-direction: column;  align-items: center; justify-content: center;border-radius: 0rem 1rem 1rem 0rem;" >
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

#medModal {
  display: none;
}

#scheduler {
  display: none;
}

#calendarNotification {
  display: none;
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
