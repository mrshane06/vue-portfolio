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

     <section id="project">
      <h1 class="projectsHead"><em>My Projects</em></h1>
      <hr>
      <div class="projects">
        <section id="proj-card" v-for="projects in projectsData()" :key="projects">
        <projects-comp>
          <template #Pimage>
            <img :src="projects.Pimage" class="project-image" >
          </template>
          <template #Pname>
            <h4 class="project-title">{{ projects.Pname }}</h4>
          </template>
          <template #description>
            <h6 class="project-text">{{ projects.description }}</h6>
          </template>
          <template #github>
            <button class="project-btn1"><a :href="projects.github" target="_blank">Github</a></button>
          </template>
          <template #live>
            <button class="project-btn2"><a :href="projects.live" target="_blank">Hosted</a></button>
          </template>
        </projects-comp>
      </section>
      </div>
     </section>

     <section id="testimonials">
      <h1 class="testiHead"><em>Testimonials</em></h1>
      <hr>
      <div class="testimonials">
        <section class="testi-card" v-for="testimonials in testimonialsData()" :key="testimonials">
          <testimonials-comp>
            <template #person_img>
              <img :src="testimonials.person_img" class="testi-img">
            </template>
            <template #name>
              <h4 class="testi-title">{{ testimonials.name }}</h4>
            </template>
            <template #testimony>
              <h6 class="testi-test">{{ testimonials.testimony }}</h6>
            </template>
          </testimonials-comp>
        </section>
      </div>
     </section>

     <hr>

     <section id="contacts">
      <h1 id="contactHead"><em>Lets Get In Contact:</em></h1>
      <div class="row">
        <div id="contactLinks">
          <p><img src="   https://cdn-icons-png.flaticon.com/512/484/484167.png " class="house"> Bonteheuwel , Cape Town</p>
          <p><img src="   https://cdn-icons-png.flaticon.com/512/1151/1151429.png " class="phone">081 421 4195</p>
        </div>
        <div >
          <img src="https://mrshane06.github.io/vue-portfolio-images/logos/Logo4.png" class="contactImg" >
        </div>
      </div>

        <section id="bam">
          <div class="col-lg-8 mt-5 mt-lg-0 mt-md-0 mt-sm-0">
            <form
             action="https://formspree.io/f/mgegqevb"
             method="POST"></form>
            <form method="post" role="form">
              <div class="row">
                <div class="col-md-6 form-group">
                  <input type="text" name="name" class="form-control" id="name" placeholder="Your Name" required>
                </div>
                <div class="col-md-6 form-group mt-3 mt-md-0">
                  <input type="email" class="form-control" name="email" id="surname" placeholder="Your Email" required>
                </div>
              </div>
              <div class="form-group mt-3">
                <textarea class="form-control" name="comments" rows="5" placeholder="Comments" required></textarea>
              </div>
              <div class="text-center mt-4 send"><button id="sub" type="submit">Submit</button></div>
            </form>
          </div>
        </section>
     </section>
     <br>
</template>
<script>
import aboutComp from '@/components/aboutComp.vue'
import navbarComp from "../components/navbarComp.vue"
import educationComp from "../components/educationComp.vue"
import skillsComp from "../components/skillsComp.vue"
import projectsComp from "../components/projectsComp.vue"
import testimonialsComp from "../components/testimonialsComp.vue"
export default {
  components:{
    navbarComp,
    aboutComp,
    educationComp,
    skillsComp,
    projectsComp,
    testimonialsComp
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
        projectsData(){
            return this.$store.state.projects
        },
        testimonialsData(){
            return this.$store.state.testimonials
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
  /* overflow: hidden; */
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

@media only screen and (max-width:400px){
  #inverse{
    display: none;
  }
  #Logo{
  width: 300px;
  height: 271px;
  display: block;
  margin: auto;
  margin-top:0px;
}
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

@media only screen and (max-width:400px){
  .aboutText{
  margin-top: 20px;
  border: 2px solid black;
  border-radius: 50px;
  margin-left: 0px;
  background-color: #2c3e50;
  color: #b3cf99;
  padding: 20px;
  place-items: center;
}
#pic1{
  margin-top:0px;
  margin-bottom:20px;
  height: 300px;
  width: 250px;
}
}
@media only screen and (max-width:300px){
  .aboutText{
  margin-top: 10px;
  border: 2px solid black;
  border-radius: 50px;
  background-color: #2c3e50;
  color: #b3cf99;
  padding: 20px;
  place-items: center;
  font-size: small;
}
#pic1{
  margin-top:0px;
  margin-bottom:20px;
  height: 300px;
  width: 250px;
}
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
}

@media only screen and (max-width:400px){
  .skill{
    display:grid;
    grid-template-columns:repeat(1,1fr);
    text-decoration: none;
    place-content: center;
  }
  #pic3{
    width: 200px;
    height: 250px;
    place-content: center;
    margin-right: 10px;
  }
}
@media only screen and (max-width:300px){
  .card{
    margin-left: 10px;
  }
  .skill-img{
  width: 223px;
  height: 140px;
  border-radius: 30px;
  }
}

/* projects section */

.projectsHead{
  padding: 30px;
}

.projects{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  text-decoration: none;
}

#proj-card{
  background-color: white;
  box-shadow: black 5px 5px 5px , -1px -1px 2px;
  width: 18rem; 
  height: 26rem;
  margin-bottom: 50px;
  margin-left: 100px;
  border-radius: 10px;
}

.project-image{
  width: 288px;
  height: 230px;
}

.project-title{
  padding-top: 16px;
  padding-bottom: 10px;
}

.project-text{
  padding: 10px;
  padding-bottom: 15px;
}

.project-btn1{
  padding: 10px;
  border-radius: 50px;
  background-color: #ccd8c1;
  margin-right: 15px;
}

.project-btn1 a{
  text-decoration:none;
  color: #2c3e50;
}

.project-btn2{
  padding: 10px;
  border-radius: 50px;
  background-color: #ccd8c1;
  margin-left: 15px;
}

.project-btn2 a{
  text-decoration: none;
  color: #2c3e50;
}

@media only screen and (max-width:400px){
  .projects{
    display:grid;
    grid-template-columns:repeat(1,1fr);
    text-decoration: none;
    place-content: center;
    margin-right: 100px;
  }

  #proj-card{
  background-color: white;
  box-shadow: black 5px 5px 5px , -1px -1px 2px;
  width: 16rem; 
  height: 25rem;
  margin-bottom: 50px;
  margin-left: 100px;
  border-radius: 10px;
}

.project-image{
  width: 240px;
  height: 200px;
  padding-top: 10px;
}

.project-title{
  padding-top: 16px;
  padding-bottom: 10px;
}

.project-text{
  padding: 10px;
  padding-bottom: 15px;
}

.project-btn1{
  padding: 10px;
  border-radius: 50px;
  background-color: #ccd8c1;
  margin-right: 15px;
}

.project-btn1 a{
  text-decoration:none;
  color: #2c3e50;
}

.project-btn2{
  padding: 10px;
  border-radius: 50px;
  background-color: #ccd8c1;
  margin-left: 15px;
}

.project-btn2 a{
  text-decoration: none;
  color: #2c3e50;
}

}

/* testimonials section */

.testiHead{
  padding: 30px;
}

.testimonials{
  display:grid;
  grid-template-columns:repeat(3,1fr)
}

.testi-card{
  background-color: white;
  box-shadow: black 5px 5px 5px , -1px -1px 2px;
  width: 20rem; 
  height: 33rem;
  margin-bottom: 50px;
  margin-left: 100px;
  border:solid 2px black;
  border-radius:10px;
}

.testi-img{
  width: 280px;
  height: 330px;
  padding-top: 20px;
}

.testi-title{
  padding: 10px;
}

.testi-test{
  padding: 10px;
  padding-bottom: 0px;
}

@media only screen and (max-width:400px){
  .testimonials{
    display:grid;
    grid-template-columns:repeat(1,1fr);
    text-decoration: none;
    place-content: center;
    margin-right: 100px;
  }
  .testi-card{
  background-color: white;
  box-shadow: black 5px 5px 5px , -1px -1px 2px;
  width: 18rem; 
  height: 32rem;
  margin-bottom: 50px;
  margin-left: 100px;
  border:solid 2px black;
  border-radius:10px;
  }
  .testi-img{
  width: 240px;
  height: 330px;
  padding-top: 20px;
  }
  .testi-test{
  padding: 10px;
  padding-bottom: 0px;
  font-size: small;
  }
}

@media only screen and (max-width:300px){
  .testimonials{
    display:grid;
    grid-template-columns:repeat(1,1fr);
    text-decoration: none;
    place-content: center;
  }
  .testi-card{
  background-color: white;
  box-shadow: black 5px 5px 5px , -1px -1px 2px;
  width: 16rem; 
  height: 32rem;
  margin-bottom: 50px;
  margin-left: 100px;
  border:solid 2px black;
  border-radius:10px;
  }
  .testi-img{
  width: 240px;
  height: 330px;
  padding-top: 20px;
  }
  .testi-test{
  padding: 10px;
  padding-bottom: 0px;
  font-size: small;
  }
}

/* contacts section */

#contactHead{
  padding-top: 10px;
  padding-bottom: 30px;
}

#contactLinks{
  border: 2px solid black;
  width: 250px;
  padding: 10px;
  margin: auto;
}

.house{
  width: 20px;
  height: 20px;
  border-radius: 100%;
}

.phone{
  width: 20px;
  height: 20px;
  border-radius: 100%;
}

#bam{
    font-family:Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    display: flex;
    justify-content: center;
}

#sub{
    width: 60px;
}

@keyframes cont{
  100% {transform: rotate(360deg);}
}

.contactImg{
  width: 155px;
  height: 140px;
  animation: rotate 5s infinite ease;
  place-items: center;
}
</style>