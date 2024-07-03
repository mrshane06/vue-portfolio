<template>
    <navbar-comp>
      <!-- <router-view/> -->
    </navbar-comp>
    <section id="home">
      <div id="links">
        <p><a href="https://github.com/mrshane06" target="_blank"><img src="https://mrshane06.github.io/vue-portfolio-images/logos/github%20logo.png"  class="git1" ></a></p>
        <p><a href="https://www.linkedin.com/in/keegan-niekerk-bb1278309/" target="_blank"><img src="https://mrshane06.github.io/vue-portfolio-images/logos/linkedin.png"  class="linkedin" ></a></p>
      </div>
    <div class="row">
      <div class="col-md-2 col-sm-12">
        <img src="https://mrshane06.github.io/vue-portfolio-images/logos/Left.png" id="inverse">
      </div>
      <div  class="col-md-8 col-sm-12">
        <img src="https://mrshane06.github.io/vue-portfolio-images/logos/Logo4.png" id="Logo">
      </div>
    </div>
        <div>
          <h2>Hello there , my name is <em>Keegan Niekerk:</em></h2>
          <br>
          <h2>and I am an Aspiring Fullstack Developer.</h2>
          <br>
          <br>
          <button class="but1" > <a href="#about">Scroll Down For More ☻</a></button>
        </div>
        <br><br>
        <hr>
    </section>

    <section id="about">
        <h1 class="aboutHead"><em>About Me</em></h1>
        <hr>
        <section id="colorAbout" v-for="about in aboutData()" :key="about">
          <div class="row">    
            <div class="col-md-3 col-sm-12">
              <about-comp>
                  <template #about>
                    <img :src='about.me' id="me">
                  </template>
              </about-comp>
            </div>
            <div class="col-md-6 col-sm-12">
                <about-comp>
                  <template #about>
                    <h4 class="aboutText">{{about.about}}</h4>
                  </template>
              </about-comp>
            </div>
            <div class="col-md-3 col-sm-12">
              <img src="https://mrshane06.github.io/vue-portfolio-images/logos/right.png" id="pic1">
            </div>
          </div>
        </section>
     </section>

     <section id="resume">
      <h1 class="resumeHead"><em>My Resume</em></h1>
      <br>
      <h2>Education:</h2>
      <div class="row">
        <div class="col-md-2 col-sm-12">
          <img src="https://mrshane06.github.io/vue-portfolio-images/logos/pic3-removebg-preview.png" id="pic3">
        </div>
        <div  class="col-md-8 col-sm-12">
          <section class="edu" v-for="education in educationData()" :key="education">
            <education-comp>
              <template #education>
               <h4>{{education.education}}</h4>
              </template>
              <br>
              <template #image>
                <img :src='education.image' class="eduImg">
              </template>
              <br>
              <template #years>
                <h4>{{education.years}}</h4>
              </template>
            </education-comp>
          </section>
        </div>
      </div>
      <br>

      <h2 class="mySkl">My Skills</h2>
      <div class="skill" >
      <section v-for="skills in skillsData()" :key="skills">
            <skills-comp>
          <!-- <template #skill>
            <h4>{{skills.skill}}</h4>
          </template>
          <template #img>
            <img :src='skills.img' class="eduImg">
          </template>
          <template #level>
            <h6 class="skill-lvl">{{skills.level}}</h6>
          </template> -->
        <template #skill>
          <div class="card" style="">
            <img :src='skills.img' class="skill-img">
            <hr>
            <div class="card-body">
              <h4 class="card-title">{{ skills.skill }}</h4>
              <h6 class="card-text">{{ skills.level }}</h6>
            </div>
          </div>
        </template>
        </skills-comp>
      </section>
      </div>
     </section> 

</template>
<script>
import aboutComp from '@/components/aboutComp.vue'
import navbarComp from "../components/navbarComp.vue"
import educationComp from "../components/educationComp.vue"
import skillsComp from "../components/skillsComp.vue"
export default {
  components:{
    navbarComp,
    aboutComp,
    educationComp,
    skillsComp,
  },
  methods:{
        aboutData(){
            return this.$store.state.about
        },
        educationData(){
            return this.$store.state.education
        },
        skillsData(){
            return this.$store.state.skills
        },
    },
    computed:{
        getData(){
            return this.$store.dispatch ('getData')
        }
    },
    mounted(){
        this.getData
    }
}
</script>
<style scoped>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* home section */

.but1{
  width: 200px;
  background-color: #b3cf99;
  color: #2c3e50;
}

.but1 a{
  text-decoration: none;
  color: #2c3e50;
}

.but1:hover{
  background-color: #bef093;
  color: #1480ec;
  box-shadow: #9bc07b 7px 7px 7px;
}

@keyframes rotate{
  100% {transform: rotate(360deg);}
}

#Logo{
  width: 300px;
  height: 271px;
  display: block;
  margin: auto;
  margin-top:80px;
  animation: rotate 5s infinite ease;
  place-items: center;
}

#links{
  display: flex;
  justify-content: flex-end;
  margin-top: 80px;
}

.linkedin{
    width: 30px;
    height: 30px;
    margin: 10px;
    border-radius: 100%
}

.git1{
    width: 30px;
    height: 30px;
    margin: 10px;
    border-radius: 100%;
}

#inverse{
  height: 330px;
  width: 260px;
  margin-top:40px;
}

/* about section */
.aboutHead{
  padding: 30px;
  background-color:#9dc775;
}

hr{
  font-weight: bold;
  color: #2c3e50;
}

#colorAbout{
  background-color:#9dc775;
}

.aboutText{
  margin-top: 80px;
  border: 2px solid black;
  border-radius: 50px;
  margin-left: 30px;
  background-color: #2c3e50;
  color: #b3cf99;
  padding: 30px;
  place-items: center;
}

#me{
  margin-top:40px;
  margin-bottom:20px;
  width: 250px;
  height:300px
}

#pic1{
  margin-top:40px;
  margin-bottom:20px;
  height: 300px;
  width: 250px;
}
/* resume section */

#resume{
  padding: 30px;
}

#pic3{
  height: 500px;
  width: 400px;
}

.eduImg{
  width: 100px;
  height: 100px;
  padding: 10px;
}

.skill{
  display:grid;
  grid-template-columns:repeat(4,1fr)
}

.mySkl{
  margin-bottom: 50px;
}

.card-title{
  padding: 10px;
  width: 220px;
  height: 50px;
}

.card-text{
  padding-bottom: 20px;
  width: 220px;
  height: 50px;
}

.skill-img{
  width: 223px;
  height: 120px;
  border-radius: 30px;
}

.card{
  box-shadow: black 5px 5px 5px , -1px -1px 2px;
  width: 14rem; 
  border-radius: 30px;
  margin-bottom: 50px;
  margin-left: 60px;
  display: flex;
  justify-content: space-around;
}

/* projects section */

/* testimonials section */

/* contacts section */

</style>
