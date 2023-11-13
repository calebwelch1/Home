<script lang="ts">

export default {
  data() {
    return { 
      showAbout:false,
      currentMessageArr: [
      ],
      patientMessages: [],
      messageArr1: [
      {message: "You have a new result from your recent visit, please visit results to view your information", sender: "health"},
      ],
      messageArr2: [],
      messageArr3: [],
      // messages is array of objects, message: "message", sender: "health" or "patient"
      currentMessage: 0,
      
     }
  },
  mounted() {
    this.currentMessageArr = this.messageArr1;
  },
  methods: {
    SetMessage(num: number) {

    }
},
  };
</script>

<template>
    <div class="dashboard">
        <h2 style="color: black; font-size: 2.5rem; margin-left: 2.5rem; margin-top: 0px;">Messages</h2>
        <div class="drop-shadow-xl absolute tag-card"
        style="left: 4%; top: 7%; color: black; border-radius: 1rem; width: 88%; height: 45rem;">
          <div style="display:flex; height: 90%; width: 90%; margin-left: 5%; margin-top: 2.5%; gap: 2%;">
            <!-- chat message titles -->
            <div style="flex: 30; background: #fff; width: 100%; height: 100%; display: flex; flex-direction: column; justify-content: flex-start; gap: 0;">
              <div class="message-box" @click="SetMessage(1)">
                <div class="icon-text-row">                
                  <span class="material-symbols-outlined" style="margin-right:0.5rem;margin-top:-0.2rem;">
                    chat_bubble
                  </span>
                  <p class="message-header">Message from Dr. Ramani</p>
              </div>
              </div>
              <div class="message-box" @click="SetMessage(2)">
                <div class="icon-text-row">                
                  <span class="material-symbols-outlined" style="margin-right:0.5rem;margin-top:-0.2rem;">
                    chat_bubble
                  </span>
                <p class="message-header">Your Test Results</p>
                </div>
              </div>
              <div class="message-box" @click="SetMessage(3)">
                <div class="icon-text-row">                
                  <span class="material-symbols-outlined" style="margin-right:0.5rem;margin-top:-0.2rem;">
                    chat_bubble
                  </span>
                  <p class="message-header">Your Appointment Details</p>
                </div>
              </div>
            </div>
            <!-- chat -->
            <div style="flex: 70; background: #7d7d7d;; width: 100%; height: 100%;  display: flex; flex-direction: column; justify-content: flex-start;">
              <div 
              :class="currentMessageArr.sender === 'health' ? 'healthMessage' : 'patientMessage'"
              v-for="(message, index) in currentMessageArr" :key="index"
              >
                <p>{{message.message}}</p>
              </div>
              </div>
            </div>
            </div>
          </div>
</template>
<style lang="scss">
.chat-bubble-med {
  
}
.message-header {
  text-align: center;
}

.icon-text-row {
  display: flex; flex-direction: row; width: 80%; padding-left: 10%; padding-right: 10%; padding-top: 7%; padding-bottom: 5%;
  justify-content: left;
}

.message-box {
  width: 100%;
  height: 100%;
  max-height: 100px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  cursor: pointer;
  border-radius: 1rem;
  margin-bottom: 4%;
}

.message-box:hover {
  background-color: #ededed
}

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
</style>
