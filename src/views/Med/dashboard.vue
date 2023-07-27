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
        <h2 style="color: black; font-size: 2.5rem; margin-left: 2.5rem; margin-top: 0%; padding-top: 2%">MyHealth Dashboard</h2>
        <div
        class="drop-shadow-xl absolute tag-card"
        style="left: 3%; top: 10%; width: 18%;">
        <div style="display: flex; flex-direction: row; width: 80%; padding-left: 10%; padding-right: 10%; padding-top: 7%; padding-bottom: 5%;">
            <div style="display: flex; flex-direction: column; position: relative; flex-grow: 1;">
                <p style="color: black; margin-top: -5%; font-size: 1.2rem; font-weight: 500; color:#3b3b3b">Balance</p>
                <p style="color: black; margin-top: 5%; font-size: 1.2rem;"> $7251.43</p>
                <!-- <p style="color: #4cc650; margin-top: 5%; font-size: 1.2rem; position: absolute; bottom: 4%; right: -25%;"> +27%</p> -->
            </div>
            <div class="brand-gradient" style="border-radius: .5rem; width: 3.1rem; height: 3.1rem; margin-left: 23%; margin-top: -2%;">
                <span class="material-symbols-outlined" style="margin-top: 15%; margin-left: 18%; color: #fff;">
                    payments
                </span>
            </div>
        </div>
        </div>
        <div
        class="drop-shadow-xl absolute tag-card"
        style="left: 24%; top: 10%; width: 18%;">
        <div @click="$emit('switchView', 'Messages')" style="display: flex; flex-direction: row; width: 80%; padding-left: 10%; padding-right: 10%; padding-top: 7%; padding-bottom: 5%; cursor: pointer;">
            <div style="display: flex; flex-direction: column; position: relative; flex-grow: 1;">
                <p style="color: black; margin-top: -5%; font-size: 1.2rem; font-weight: 500; color:#3b3b3b">Messages</p>
                <p style="color: black; margin-top: 5%; font-size: 1.2rem;"> 2 Messages</p>
            </div>
            <div class="brand-gradient" style="border-radius: .5rem; width: 3.1rem; height: 3.1rem; margin-left: 23%; margin-top: -2%;">
                <span class="material-symbols-outlined" style="margin-top: 15%; margin-left: 18%; color: #fff;">
                    mail
                </span>
            </div>
        </div>
        </div>
        <div
        class="drop-shadow-xl absolute tag-card"
        style="left: 3%; top: 21%; width: 18%;">
        <div @click="$emit('switchView', 'Health')" style="display: flex; flex-direction: row; width: 80%; padding-left: 10%; padding-right: 10%; padding-top: 7%; padding-bottom: 5%; cursor: pointer;">
            <div style="display: flex; flex-direction: column; position: relative; flex-grow: 1;">
                <p style="color: black; margin-top: -5%; font-size: 1.2rem; font-weight: 500; color:#3b3b3b">Medication</p>
                <p style="color: black; margin-top: 5%; font-size: 1.2rem;"> 4 Refills</p>
                <!-- <p style="color: #4cc650; margin-top: 5%; font-size: 1.2rem; position: absolute; bottom: 4%; right: -25%;"> +27%</p> -->
            </div>
            <div class="brand-gradient" style="border-radius: .5rem; width: 3.1rem; height: 3.1rem; margin-left: 23%; margin-top: -2%;">
                <span class="material-symbols-outlined" style="margin-top: 15%; margin-left: 18%; color: #fff;">
                    pill
                </span>
            </div>
        </div>
        </div>
        <div
        class="drop-shadow-xl absolute tag-card"
        style="left: 24%; top: 21%; width: 18%;">
        <div @click="$emit('switchView', 'Health')" style="display: flex; flex-direction: row; width: 80%; padding-left: 10%; padding-right: 10%; padding-top: 7%; padding-bottom: 5%; cursor: pointer;">
            <div style="display: flex; flex-direction: column; position: relative; flex-grow: 1;">
                <p style="color: black; margin-top: -5%; font-size: 1.2rem; font-weight: 500; color:#3b3b3b">Test Results</p>
                <p style="color: black; margin-top: 5%; font-size: 1.2rem;"> 3 Results</p>
                <!-- <p style="color: #4cc650; margin-top: 5%; font-size: 1.2rem; position: absolute; bottom: 4%; right: -25%;"> +27%</p> -->
            </div>
            <div class="brand-gradient" style="border-radius: .5rem; width: 3.1rem; height: 3.1rem; margin-left: 23%; margin-top: -2%;">
                <span class="material-symbols-outlined" style="margin-top: 15%; margin-left: 18%; color: #fff;">
                    science
                </span>
            </div>
        </div>
        </div>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 3%; top: 36%; color: black; border-radius: 1rem; width: 39%; height: 16rem;">
          <div id="health-notification-container" style="margin-left: 5%; margin-top: 5%; width: 90%; height: 74%; position: relative; background: #f7f7f7; border-radius: 1rem; overflow-y: scroll; overflow-x: hidden;">
            <div @click="$emit('switchView', 'Health')" class="health-notification">
              <div class="brand-gradient" style="border-radius: 1rem; width: 2.3rem; height: 2.3rem; margin-top: 0.4%;">
                <span class="material-symbols-outlined" style="font-size: 0.8rem; margin-top: 2%; margin-left: 2%; color: #fff;">
                  science
                </span>
            </div>
            <p style="font-size: 1rem; padding-top: 2.5%; width: 50%;">
                  You have new or modified test results.
            </p>
            <button style="color: #fff; width: 28%; height: 36%; border-radius: 0.25rem; font-size: 1rem; font-weight: 600; border: none; background:#fc2e20; margin-top: 2.5%;">View Results</button>
            </div>
            <!--  -->
            <div @click="$emit('switchView', 'Health')" class="health-notification">
              <div class="brand-gradient" style="border-radius: 1rem; width: 2.3rem; height: 2.3rem; margin-top: 0.4%;">
                <span class="material-symbols-outlined" style="font-size: 0.8rem; margin-top: 2%; margin-left: 2%; color: #fff;">
                  pill
                </span>
            </div>
            <p style="font-size: 1rem; padding-top: 2.5%; width: 50%;">
                  Medications available for refill.
            </p>
            <button style="color: #fff; width: 28%; height: 36%; border-radius: 0.25rem; font-size: 1rem; font-weight: 600; border: none; background:#fc2e20; margin-top: 2.5%;">Medication</button>
            </div>
            <!--  -->
            <div @click="$emit('switchView', 'Benefits')" class="health-notification">
              <div class="brand-gradient" style="border-radius: 1rem; width: 2.3rem; height: 2.3rem; margin-top: 0.4%;">
                <span class="material-symbols-outlined" style="font-size: 0.8rem; margin-top: 2%; margin-left: 2%; color: #fff;">
                  payments
                </span>
            </div>
            <p style="font-size: 1rem; padding-top: 2.5%; width: 50%;">
                  View your new benefits.
            </p>
            <button style="color: #fff; width: 28%; height: 36%; border-radius: 0.25rem; font-size: 1rem; font-weight: 600; border: none; background:#fc2e20; margin-top: 2.5%;">View Benefits</button>
            </div>
            <!--  -->
            <div @click="$emit('switchView', 'Health')" class="health-notification">
              <div class="brand-gradient" style="border-radius: 1rem; width: 2.3rem; height: 2.3rem; margin-top: 0.4%;">
                <span class="material-symbols-outlined" style="font-size: 0.8rem; margin-top: 2%; margin-left: 2%; color: #fff;">
                  science
                </span>
            </div>
            <p style="font-size: 1rem; padding-top: 2.5%; width: 50%;">
                  You have new or modified test results.
            </p>
            <button style="color: #fff; width: 28%; height: 36%; border-radius: 0.25rem; font-size: 1rem; font-weight: 600; border: none; background:#fc2e20; margin-top: 2.5%;">View Results</button>
            </div>
          </div>
        </div>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 50%; top: 10%; color: black; border-radius: 1rem; width: 39%; height: 50%;">
        <h2 style="color: black; font-size: 1.8rem; margin-left: 8%; margin-top: 5%;">Finish Setting Up Your Profile</h2>
          <div style="margin-left: 10%; width: 85%; height: 74%; position: relative;">
            <div class="progress-bar">
            <div class="dot-one active" style="top: -2%;"></div>
            <div class="dot-two" style="top: 10%;"></div>
            <div class="dot-three" style="top: 66%;"></div>
            <div class="dot-three" style="top: 82%;"></div>
            <div class="progress-line" style="height: 30%;"></div>
            </div>
            <p style="position: absolute; z-index:10; top: -1%; left: 10%; color:#5d5d5d; font-weight: 600;">Create your account</p>
            <p style="position: absolute; z-index:10; top: 12%; left: 10%; color:#3b3b3b; font-weight: 600;">Connect a source</p>
            <p style="position: absolute; z-index:10; top: 22%; left: 10%; color:#787878; font-size: 1.2rem;">Lorem ipsum dolor consceptor idipsing <br> al tim et. inseptim qalmri setentum <br> quaranme recept limori</p>
            <button class="green-gradient" style="position: absolute; z-index:10; top: 45%; left: 10%; color: #fff; width: 38%; height: 12%; border-radius: 0.5rem; font-size: 1.1rem; font-weight: 600; border: none;">Connect</button>
            <p style="position: absolute; z-index:10; top: 68%; left: 10%; color:#787878; font-size: 1.2rem;">Lorem ipsum dolor consceptor idipsing</p>
            <p style="position: absolute; z-index:10; top: 84%; left: 10%; color:#787878; font-size: 1.2rem;">At vero eos et accusamus et iusto odio <br> dignissimos ducimus qui blanditiis praesentium </p>
          </div>
        </div>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 20%; top: 66%; color: black; border-radius: 1rem; width: 54%; height: 10rem;">
        <div style="display: flex; flex-direction: row; width: 100%; padding-left: 0%; padding-right: 10%; padding-top: 7%; padding-bottom: 5%; border: 1px solid red;">
          <div class="brand-gradient" style="border-radius: .5rem; width: 3.1rem; height: 3.1rem; margin-left: 23%; margin-top: -2%;">
                <span class="material-symbols-outlined" style="margin-top: 15%; margin-left: 18%; color: #fff;">
                    breaking_news
                </span>
            </div>
            <div style="display: flex; flex-direction: column; position: relative; flex-grow: 1;">
                <p style="color: black; font-size: 1.2rem;"> At vero eos et accusamus et iusto odio <br> dignissimos ducimus qui blanditiis praesentium </p>
                <!-- <p style="color: #4cc650; margin-top: 5%; font-size: 1.2rem; position: absolute; bottom: 4%; right: -25%;"> +27%</p> -->
            </div>
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
    // width: 18rem;
    // width: 1%;
    height: 5rem;
}

.brand-gradient {
  background: rgb(255,27,24);
  background: linear-gradient(342deg, rgba(255,27,24,1) 0%, rgba(255,149,0,1) 100%, rgba(0,212,255,1) 100%);
}

.green-gradient {
  background: rgb(42,199,123);
  background: linear-gradient(90deg, rgba(42,199,123,1) 0%, rgba(76,203,76,1) 100%, rgba(12,215,96,1) 100%);
}

.progress-bar {
    display: flex;
    flex-direction: column;
    align-items: center;
    position: relative;
    width: 4px;
    height: 100%;
    background-color: #ddd;
}

.dot-one {
    width: 19px;
    height: 19px;
    border-radius: 50%;
    margin: 5px 0;
    background-color: #ccc;
    position: absolute;

}

.dot-two {
    width: 19px;
    height: 19px;
    border-radius: 50%;
    margin: 5px 0;
    background-color: #fff;
    border: 3px solid #ccc;
    position: absolute;

}

.dot-three {
    width: 19px;
    height: 19px;
    border-radius: 50%;
    margin: 5px 0;
    background-color: #fff;
    border: 3px solid #ccc;
    position: absolute;
}

.progress-line {
    position: absolute;
    border: 1px solide red;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 4px;
    // height: 100%;
    background-color: #3498db;
    z-index: -1;
}

.active {
    background-color: #27ae60;
    border: 3px solid #27ae60;
}

.health-notification {
  border: 1px solid #f7f7f7;
  display: flex; flex-direction: row;
  width: 100%;
  height: 29%;
  gap: 6%;
  padding-top: 1%;
  border-radius: 1rem;
}

.health-notification:hover {
  border: 1px solid #b5b5b5;
  cursor: pointer;
}
</style>
