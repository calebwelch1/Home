<script lang="ts">
import Dashboard from './Med/dashboard.vue';

export default {
    components : {
        Dashboard,
    },
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
  <main>
    <html lang="en">
<body>
    <div class="container">
        <div class="first-div">
            <!--  -->
            <div class="I AM THE SPACER!!!!" style="height: 2vh;" />
            <!--  -->
            <div class="drop-shadow-xl" style="margin-left: 20px; background: #fff; border-radius: 1rem; width: 85%; display:flex; flex-direction: row; padding-top: 1rem; padding-bottom: 1rem;">
                <div style="background:#fc2e20; border-radius: .5rem; width: 2.5rem; height: 2.5rem;margin-left: 20px;">
                <span class="material-symbols-outlined" style="margin-top: 0.25rem; margin-left: 0.25rem;">
                    view_cozy
                </span>
                </div>
                <p style="color:black; margin-left: 1rem; font-size: 1.3rem; font-weight: 300; margin-top: 0.45rem;">Current View</p>
                <p style="color:black; margin-left: 1rem; font-size: 2rem; margin-top:-0.4rem;">&#8964;</p>
                <!-- TODO: make it dynamic! -->
            </div>
            <ul class="flex-list">
                <li class="menu-item">
                    <span class="material-symbols-outlined position-menu-items">
                        home
                    </span>
                    <p class="position-menu-items position-menu-item-p">Home</p>
                </li>
                <li class="menu-item">
                    <span class="material-symbols-outlined position-menu-items">
                        home
                    </span>
                    <p class="position-menu-items position-menu-item-p">Health</p>
                </li>
                <li class="menu-item">
                    <span class="material-symbols-outlined position-menu-items">
                        home
                    </span>
                    <p class="position-menu-items position-menu-item-p">Benefits</p>
                </li>
                <li class="menu-item">
                    <span class="material-symbols-outlined position-menu-items">
                        home
                    </span>
                    <p class="position-menu-items position-menu-item-p">History</p>
                </li>
                <li class="menu-item">
                    <span class="material-symbols-outlined position-menu-items">
                        home
                    </span>
                    <p class="position-menu-items position-menu-item-p">Profile</p>
                </li>
            </ul>
            <!--  -->
            <div class="I AM THE SPACER!!!!" style="height: 38vh;" />
            <!--  -->
            <div style="position: relative;">
            <p style="color: black; position: absolute; top: -10%; right: 13%; font-size: 14px; font-weight: 600;">tm</p>
            <h1 style="color:#fc2e20; padding-left: 40px; font-size: 2.8rem;">MyHealth+</h1>
            </div>
        </div>
        <div class="second-div">
            <div style="background: #f7f7f7; height: 7rem; display: flex; flex-direction:row;">
                <div style="position: relative;">
                <p style="color: black; position: absolute; top: 10%; right: -2%; font-size: 14px; font-weight: 600;">tm</p>
                <h1 style="color:#fc2e20; padding-left: 40px; font-size: 2.8rem;">MyHealth+</h1>
                </div>
                <!--  -->
                <div style="display: flex; flex-direction: row; margin-left: 65%; margin-top: 2.5%; margin-bottom: 2.5%;">
                <span class="material-symbols-outlined" style="color: #545454;">
                person
                </span>
                <p style="color:#545454; margin-left: 1rem; margin-right: 1rem; font-size: 1.3rem; margin-top: 3%;">Guest</p>
                <p style="color:#545454; margin-left: -10px; margin-right: 1rem; font-size: 2.2rem; margin-top: -5%;">&#8964;</p>
                <span class="material-symbols-outlined" style="color: #545454; margin-top: 1%;">
                notifications
                </span> 
                </div>
            </div>
            <Dashboard />
        </div>
    </div>
</body>
</html>
  </main>
</template>
<style lang="scss">
body,
html {
  height: 100%;
  background: #110101;
  font-family: 'Roboto', sans-serif;
  overflow: hidden;
}

p {
    margin: 0px;
}

.container {
  display: flex;
  height: 100%;
  width: 100%;
  padding: 0px;
  overflow: hidden;
}

.first-div {
  flex: 17;
  background-color: #ededed;
  position: relative;
}

.second-div {
  flex: 83;
  background-color: #f0f0f0;
  overflow: hidden;
}

.sidebar {
        min-width: 20vw;
        max-width: 20vw;
        width: 20vw;
        min-height: 100vh;
        background-color: blueviolet;
        margin-right: 0px;
      }

.main {
    min-height: 100vh;
    min-width: 79vw;
    max-width: 79vw;
    background: forestgreen;
}

.menu-item {
    width: 100%;
    height: 4rem;
    color: #8e8e8e;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    grid-auto-rows: minmax(10px, auto);
    font-size: 1.4rem;
    padding-top: 0.5rem;
}

.position-menu-items {
    grid-column: 1/3;
  grid-row: 2 / 5;
}

.position-menu-item-p {
    margin-left: 3rem; margin-top: 0.4rem;
}

.menu-item:hover {
    cursor: pointer;
    color: #fc2e20;
    // background: #8e8e8e;
}

.material-symbols-outlined {
        font-variation-settings:
        'FILL' 0,
        'wght' 400,
        'GRAD' 0,
        'opsz' 48;
        font-size: 2rem !important;
}

.flex-list {
  display: flex;
  flex-direction: column;
  list-style: none;
}

.position-icon {
    position: absolute;
    top: 50%;
    left: 10%;
}

.drop-shadow-xl {
    filter: drop-shadow(0 20px 13px rgb(0 0 0 / 0.03)) drop-shadow(0 8px 5px rgb(0 0 0 / 0.08));
}
</style>
