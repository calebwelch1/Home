<script lang="ts">
interface MessageArrType {
    message: any;
    sender: string;
  }

export default {
  data() {
    return { 
      showAbout:false,
      currentMessageArr: [] as MessageArrType[],
      patientMessages: [],
      messageArr1: [
      {message: "You have a new result from your recent visit, please visit health results to view your information", sender: "health"},
      ],
      messageArr2: [
      {message: "You have a new statement, please visit billing to pay or create a payment plan", sender: "health"},
      ],
      messageArr3: [
      {message: "Our clinic at 555 Hospital St. will be under construction this summer, please visit news to plan ahead for your next visit", sender: "health"},
      ],
      // messages is array of objects, message: "message", sender: "health" or "patient"
      currentMessage: 0,
      
     }
  },
  mounted() {
    this.currentMessageArr = this.messageArr1;
  },
  methods: {
    SetMessageArr(num: number) {
      this.RemoveActiveTitles();
      switch(num){
        case 1:
          this.SetActiveTitle(1)
          this.currentMessageArr = this.messageArr1;
          break;
        case 2:
          this.SetActiveTitle(2)
          this.currentMessageArr = this.messageArr2;
          break;
        case 3:
          this.SetActiveTitle(3)
          this.currentMessageArr = this.messageArr3;
          break;
        default:
          this.currentMessageArr = this.messageArr1;
          break;
      }
    },
    SetActiveTitle(num: number){
      const title = document.getElementById(`message-title-${num}`);
      title!.style.backgroundColor = "#ededed";
    },
    RemoveActiveTitles(){
      for (let i = 1; i < 4; i++){
      const title = document.getElementById(`message-title-${i}`);
      title!.style.backgroundColor = "";
      }
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
              <div id="message-title-1" class="message-box" @click="SetMessageArr(1)">
                <div class="icon-text-row">                
                  <span class="material-symbols-outlined" style="margin-right:0.5rem;margin-top:-0.2rem;">
                    chat_bubble
                  </span>
                  <p class="message-header">Message from Dr. Ramani</p>
              </div>
              </div>
              <div id="message-title-2" class="message-box" @click="SetMessageArr(2)">
                <div class="icon-text-row">                
                  <span class="material-symbols-outlined" style="margin-right:0.5rem;margin-top:-0.2rem;">
                    chat_bubble
                  </span>
                <p class="message-header">Your Test Results</p>
                </div>
              </div>
              <div id="message-title-3" class="message-box" @click="SetMessageArr(3)">
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
              :class="currentMessageArr.sender === 'health' ? 'chat-bubble health-bubble' : 'chat-bubble patient-bubble'"
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

.message-box-active {
  background-color: #ededed
}

/* Chat bubble */
.chat-bubble {
  background-color: #DCF8C6; /* Bubble background color */
  border-radius: 10px;
  padding: 10px;
  margin: 10px;
  max-width: 70%; /* Adjust as needed */
}

/* Sender's chat bubble */
.health-bubble {
  align-self: flex-end;
  background-color: #DCF8C6; /* Bubble background color */
  color: #000; /* Text color */
}

/* Receiver's chat bubble */
.patient-bubble {
  align-self: flex-start;
  background-color: #E8E8E8; /* Bubble background color */
  color: #000; /* Text color */
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
