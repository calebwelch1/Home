<script lang="ts">
import {
  Chart as ChartJS,
  CategoryScale,
  LinearScale,
  PointElement,
  LineElement,
  Title,
  Tooltip,
  Legend
} from 'chart.js'
import { Line } from 'vue-chartjs'

ChartJS.register(
  CategoryScale,
  LinearScale,
  PointElement,
  LineElement,
  Title,
  Tooltip,
  Legend
)

export default {
  components: {
    Line,
  },
  data() {
    return { 
      showAbout:false,
      data: {
        labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: [40, 39, 10, 40, 39, 80, 40]
          }
        ]
      },
      options: {
      responsive: true,
      maintainAspectRatio: false
    },
     }
  },
  mounted() { },
  methods: {
},
  };
</script>

<template>
    <div class="dashboard">
      <h2 style="color: black; font-size: 2.5rem; margin-left: 2.5rem; margin-top: 0px;">Billing</h2>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 3%; top: 10%; color: black; border-radius: 1rem; width: 60%; height: 32rem;">
          <Line :data="data" :options="options" />
        </div>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 70%; top: 10%; color: black; border-radius: 1rem; width: 20%; height: 50%;">
           health care
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
    overflow-x: scroll;
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
