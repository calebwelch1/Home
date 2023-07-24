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
        <div style="display: flex; flex-direction: row; width: 85%; padding-left: 10%; padding-right: 10%; padding-top: 7%; padding-bottom: 5%;">
            <div style="display: flex; flex-direction: column;">
                <p style="color: black; margin-top: -5%; font-size: 1.2rem; font-weight: 500; color:#3b3b3b"> Your Account</p>
                <p style="color: black; margin-top: 5%; font-size: 1.2rem;"> $7251.43</p>
            </div>
            <div class="brand-gradient" style="border-radius: .5rem; width: 3.1rem; height: 3.1rem; margin-left: 23%; margin-top: -2%;">
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
</style>
