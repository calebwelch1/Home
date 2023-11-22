<script lang="ts">
import healthBanner from './healthBanner.png'
import drinking from './assets/drinking.jpg'
import depression from './assets/depression.jpg'
import patient from './assets/patient.jpg'
export default {
  data() {
    return { 
      showAbout:false,
      healthBanner,
      news: [
        {
          Title:'TREATING HIGH-RISK DRINKING, ALCOHOL USE DISORDER: NEW CANADIAN GUIDELINE',
          Description:'A new Canadian guideline for treating high-risk drinking and alcohol use disorder (AUD) with 15 evidence-based recommendations to reduce harms associated with high-risk drinking and to support people’s treatment and recovery from AUD is published in CMAJ (Canadian Medical Association Journal).',
          Img: drinking,
          link:'https://hospitalnews.com/treating-high-risk-drinking-alcohol-use-disorder-new-canadian-guideline/',
        },
        {
          Title:'ENHANCING THE PATIENT EXPERIENCE WITH ESSENTIAL CARE PARTNER PROGRAMS',
          Description:'According to research published in the Canadian Medical Association Journal, caregivers provide approximately 75 per cent of the care delivered in our healthcare system, making their roles vital for patients’ physical, emotional, and cognitive well-being. ',
          Img: patient,
          link:'https://hospitalnews.com/enhancing-the-patient-experience-with-essential-care-partner-programs/',
        },
        {
          Title:'PHARMACOGENOMIC TESTING: PROMISING TREATMENT FOR DEPRESSION',
          Description:'Pharmacogenomic testing of adults with moderate or severe major depressive disorder (MDD) shows promise in helping select the right antidepressant, which could save health systems millions of dollars and improve survival and quality of life, according to a study from that province published in CMAJ (Canadian Medical Association Journal).',
          Img: depression,
          link:'https://hospitalnews.com/pharmacogenomic-testing-promising-treatment-for-depression/',
        },
      ]
     }
  },
  mounted() { },
  methods: {
  openInNewTab(url) {
    window.open(url, '_blank').focus();
  },
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
        <div style="overflow-y: scroll; height: 100%; display: block;">
        <div
        class="drop-shadow-xl cursor"
        @click="openInNewTab(newsItem.link)"
        style="display: flex; flex-direction: row; gap: 3rem; justify-content: space-between; height: 100%; margin-left: auto; margin-right: auto; margin-bottom: 2rem; width: 90%; max-width:100%; max-height:18rem; border-radius: 2rem; background: white; color: black;"
        v-for="(newsItem, index) in news"
        >
        <div style="flex:30;">
        <img :src="newsItem.Img" style="max-height: 350px; max-width:500px; height:100%; width:100%; border-radius: 2rem 0rem 0rem 2rem;" />
        </div>
        <div style="flex: 60; display: flex; flex-direction:column; justify-content: space-between; margin: 1.5rem;">
          <h2 style="font-size: 1.8rem;">{{newsItem.Title}}</h2>
          <p>{{newsItem.Description}}</p>
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
    height: 5rem;
}
</style>
