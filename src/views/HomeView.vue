<script lang="ts">
// import jQuery from 'jquery'
import $ from 'jquery'
// import pJs from './particles.js'
import resume from './Welch_Caleb_Full_Stack_Resume.pdf';

export default {
  data() {
    return { 
      showAbout:false,
      showContact: false,
      showWork: false,
      viewResume: false,
      resume,
     }
  },
  mounted() {
    setTimeout(function(){
    $("#loading").addClass("animated fadeOut");
    setTimeout(function(){
      $("#loading").removeClass("animated fadeOut");
      $("#loading").css("display","none");
      $("#box").css("display","none");
      $("#about").removeClass("animated fadeIn");
      $("#contact").removeClass("animated fadeIn");
      $("#work").removeClass("animated fadeIn");
    },700);
},1200);
  },
  methods: {
//     showabout(){
//     $("#about_container").css("display","inherit");
//     $("#about_container").addClass("animated slideInLeft");
//     setTimeout(() => {
//         $("#about_container").removeClass("animated slideInLeft");
//     },800);
// },
closeabout(){
    $("#about_container").addClass("animated slideOutLeft");
    setTimeout(function(){
        $("#about_container").removeClass("animated slideOutLeft");
        $("#about_container").css("display","none");
    },800);
},
showwork(){
    $("#work_container").css("display","inherit");
    $("#work_container").addClass("animated slideInRight");
    setTimeout(function(){
        $("#work_container").removeClass("animated slideInRight");
    },800);
},
closework(){
    $("#work_container").addClass("animated slideOutRight");
    setTimeout(function(){
        $("#work_container").removeClass("animated slideOutRight");
        $("#work_container").css("display","none");
    },800);
},
showcontact(){
    $("#contact_container").css("display","inherit");
    $("#contact_container").addClass("animated slideInUp");
    setTimeout(function(){
        $("#contact_container").removeClass("animated slideInUp");
    },800);
},
closecontact(){
    $("#contact_container").addClass("animated slideOutDown");
    setTimeout(function(){
        $("#contact_container").removeClass("animated slideOutDown");
        $("#contact_container").css("display","none");
    },800);
},
  },
  created() {
    // this.plus()
    // console.log(this.a) // => 2
  }
}
</script>

<template>
  <main>
    <html lang="en">
<body>
    <div id="loading">
        <div id="spinner"></div>
    </div>
    <!-- <div id="particles-js"></div> -->
    <div id="box">
        <div class="box1 onlywide animated bounceOutLeft" style="animation-delay:1.7s;"></div>
        <div class="box2 onlywide animated bounceOutLeft" style="animation-delay:1.8s;"></div>
        <div class="box2 onlywide animated bounceOutLeft" style="animation-delay:1.9s;"></div>
        <div class="box2 animated bounceOutRight" style="animation-delay:1.9s;"></div>
        <div class="box2 onlywide animated bounceOutRight" style="animation-delay:1.8s;"></div>
        <div class="box2 onlywide animated bounceOutRight" style="animation-delay:1.7s;"></div>
    </div>
    <a id="about" @click="showAbout = !showAbout" class="animated fadeIn" style="animation-delay:2.2s;">about</a>
    <a id="work" @click="showWork = !showWork" class="animated fadeIn" style="animation-delay:2.2s;">work</a>
    <a id="contact" @click="showContact = !showContact" class="animated fadeIn" style="animation-delay:2.2s;">contact</a>
    <div id="middle" class="animated slideInDown" style="animation-delay:2.0s;">
        <h1>caleb welch</h1>
        <h2>Artist /  Software Developer / Human</h2>
        <div>
          <a href="https://github.com/calebwelch1" target="_blank" class="h-3 w-3"
            style="border-radius: 9999px; margin: 1rem;">
              <img class="h-2 w-2 filter-white" src="../icons/github.png" style="margin-top:0.4rem; margin: 1rem;" alt="images made by https://www.flaticon.com"/>
            </a>
        <a href="https://www.instagram.com/therealcalebwelch/" target="_blank" class="h-3 w-3"
            style="border-radius: 9999px; margin: 1rem;">
              <img class="h-2 w-2 filter-white" src="../icons/instagram.svg" style="margin-top:0.4rem; margin: 1rem;"/>
            </a>
            <a href="https://www.linkedin.com/in/caleb-welch-502851121/" target="_blank" class="h-3 w-3"
            style="border-radius: 9999px; margin: 1rem;">
              <img class="h-2 w-2 filter-white" src="../icons/linkedin.svg" style="margin-top:0.4rem; margin: 1rem;"/>
            </a>
          </div>
        <div id="menu">
            <a @click="showAbout = !showAbout">about</a>
            <a @click="showWork = !showWork">work</a>
            <a @click="showContact = !showContact">contact</a>
        </div>
        <!-- <table>
                <tr>
                    <td class="animated zoomIn" style="animation-delay:2.2s;"><a class="social"><i class="fab fa-facebook"></i></a></td>
                    <td class="animated zoomIn" style="animation-delay:2.4s;"><a class="social"><i class="fab fa-twitter"></i></a></td>
                    <td class="animated zoomIn" style="animation-delay:2.6s;"><a class="social"><i class="fab fa-instagram"></i></a></td>
                    <td class="animated zoomIn" style="animation-delay:2.8s;"><a class="social"><i class="fab fa-dribbble"></i></a></td>
                </tr>
        </table> -->
    </div>
    <Transition name="work">
    <div v-if="showWork" id="work_container" class="container" style="display: inherit;">
        <div @click="showWork = !showWork">&gt;</div>
        <h1>works.</h1>
        <section>
            <h2>C-Collection</h2>
            <p>
               Media important to my development as a human.
            </p>
            <div id="used">
                <div><i class="fas fa-circle"></i>&nbsp;Vue 3</div>
                <div><i class="fas fa-circle"></i>&nbsp;CSS3</div>
                <div><i class="fas fa-circle"></i>&nbsp;SCSS</div>
                <div><i class="fas fa-circle"></i>&nbsp;Javascript</div>
                <div><i class="fas fa-circle"></i>&nbsp;Adobe After Effects</div>
            </div>
            <a target="_blank" href="https://calebwelch1.github.io/c-collection/" ><button class="btn_one">Visit</button></a>
        </section>
        <section>
            <h2>UI/UX</h2>
            <p>
                Figma Designs (hosted on legacy site)
            </p>
            <div id="used">
                <div><i class="fas fa-circle"></i>&nbsp;Figma</div>
                <div><i class="fas fa-circle"></i>&nbsp;Wireframing</div>
                <div><i class="fas fa-circle"></i>&nbsp;UI/UX Design</div>
            </div>
            <a target="_blank" href="https://calebwelch1.github.io/#/UIPortfolio" ><button class="btn_one">Visit</button></a>
        </section>
    </div>
  </Transition>
    <Transition name="about">
    <div v-if="showAbout" id="about_container" class="container" style="display: inherit;">
            <div @click="showAbout = !showAbout">&lt;</div>
            <h1>about.</h1>
            <section>
                <h2>about me</h2>
                <p>
                    Hey! Thanks for visiting my site. I'm a software developer based in the greater Boston area. I specialize in the front end but I am proficient in back end work as well. I'm currently collecting Amazon Web Services certifications on my journey to AWS DevOps Mastery.
                    I'm experienced in building client facing, fully custom applications with typescript, javascript, CSS, SCSS and Nodejs in an Agile Development system. Creates cloud solutions with in-depth AWS knowledge.

                </p>
            </section>
            <section>
                <h2>skills</h2>
                <p>
                  Javascript ES6 / jQuery	/ REST  / MySQL	/ Git(Git Flow)	/ React / Redux	/ Wireframing /
TypeScript	/ GraphQL	/ Github Issues	/ Vue3 / Figma /
CSS / SASS / LESS	/	SCRUM / Agile	/ AngularJS	/ Prototyping /
HTML / XHTML / Jade / NodeJS / Github / Bootstrap / Adobe Suite / Webpack / End to End Testing	/ Jira / User Stories
508 Accessibility / AWS / Atomic Design
                </p>
                <h2>resume</h2>
                <button class="btn_one" @click="viewResume = !viewResume">View Resume</button>
                <Transition name="contact">
                <iframe v-if="viewResume" :src="resume" width="100%" height="500px"></iframe>
                </Transition>
            </section>
        </div>
      </Transition>
      <Transition name="contact">
          <div v-if="showContact" id="contact_container" class="container" style="display: inherit;">
            <div @click="showContact = !showContact">v</div>
            <h1>contact.</h1>
            <section>
                <h2>contact me</h2>
                <div style="color:white;margin-top:10rem;margin-bottom:5rem;"> Email me: calebwelch.design@gmail.com </div>
            <a href="https://www.instagram.com/therealcalebwelch/" target="_blank" class="h-3 w-3"
            style="border-radius: 9999px; margin: 1rem;">
              <img class="h-2 w-2 filter-white" src="../icons/instagram.svg" style="margin-top:0.4rem; margin: 1rem;"/>
            </a>
            <a href="https://www.linkedin.com/in/caleb-welch-502851121/" target="_blank" class="h-3 w-3"
            style="border-radius: 9999px; margin: 1rem;">
              <img class="h-2 w-2 filter-white" src="../icons/linkedin.svg" style="margin-top:0.4rem; margin: 1rem;"/>
            </a>
            </section>
        </div>
      </Transition>
    <!-- <script src="index.js" type="text/javascript"></script>
    <script src="particles.js"></script>
    <script src="app.js"></script> -->
</body>
</html>
  </main>
</template>
<style>
.about-enter-active {
  transition: all 0.5s ease-out;
}

.about-leave-active {
  transition: all 0.5s ease-out;
}

.about-enter-from,
.about-leave-to {
  transform: translateX(-200px);
  opacity: 0;
}

.work-enter-active {
  transition: all 0.5s ease-out;
}

.work-leave-active {
  transition: all 0.5s ease-out;
}

.work-enter-from,
.work-leave-to {
  transform: translateX(200px);
  opacity: 0;
}


.contact-enter-active {
  transition: all 0.5s ease-out;
}

.contact-leave-active {
  transition: all 0.5s ease-out;
}

.contact-enter-from,
.contact-leave-to {
  transform: translateY(200px);
  opacity: 0;
}

.filter-white{
  filter: invert(100%) sepia(4%) saturate(7482%) hue-rotate(233deg) brightness(113%) contrast(95%);
}

.h-2 {
  height:2rem;
}

.w-2 {
  width: 2rem;
}
</style>

