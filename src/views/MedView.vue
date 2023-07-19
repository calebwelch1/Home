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
            <div>CURRENT VIEW</div>
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
        </div>
        <div class="second-div">
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
</style>
