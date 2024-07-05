<template>
      <div>
      <spinner-comp>
        
      </spinner-comp>
    </div>
    <navbar-comp>
      <router-view></router-view>
    </navbar-comp>

    <div>
      <footer-comp>

      </footer-comp>
    </div>
</template>

<script>

import footerComp from './components/footerComp.vue'
import spinnerComp from './components/spinnerComp.vue'
export default{
  components:{
    footerComp,
    spinnerComp
  }
}
</script>
<style>
body{
  background-color: #b3cf99;
  font-family:Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
  color: #2c3e50;
  text-align: center;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  overflow-x: hidden;
}

/* navbar settings */
nav {
  overflow: hidden;
  position: fixed;
  top: 0;
  width: 100%;
  background-color: #CEDECD;
  box-shadow: #9bc07b 7px 7px 7px;
  /* height: 65px; */
}

li {
  padding: 10px;
  padding-top: 15px;
  padding-bottom: 15px;
}

li a {
  color: #2c3e50;
  font-weight: bold;
}

li a:hover{
  transition: 2s ;
  color: #42b983;
  padding: 5px;
  background-color: #d1d6d4;
}

@media only screen and (max-width:400px){
  nav{
    width: 100%;
  }
}

@media only screen and (max-width:300px){
  nav{
    width: 100%;
  }
}
</style>
