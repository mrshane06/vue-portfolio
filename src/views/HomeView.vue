<template>
    <navbar-comp>
      <router-view/>
    </navbar-comp>
    <section id="home">
      <div id="links">
        <p><a href="https://github.com/mrshane06" target="_blank"><img src="https://mrshane06.github.io/vue-portfolio-images/logos/github%20logo.png"  class="git1" ></a></p>
        <p><a href="https://www.linkedin.com/in/keegan-niekerk-bb1278309/" target="_blank"><img src="https://mrshane06.github.io/vue-portfolio-images/logos/linkedin.png"  class="linkedin" ></a></p>
      </div>
    <div class="row">
      <div class="col-md-2 col-sm-12">
        <img src="https://mrshane06.github.io/vue-portfolio-images/logos/Point_Inverse-color.png" id="inverse">
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

    <!-- <section id="about">
      <h1><em>About Me</em></h1>
      <div>

      </div>
    </section> -->

</template>
<script>
import navbarComp from "../components/navbarComp.vue"
export default {
  components:{
    navbarComp
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

/* resume section */

/* projects section */

/* testimonials section */

/* contacts section */

</style>
