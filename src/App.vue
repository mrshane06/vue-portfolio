<template>
    <navbar-comp>
      <router-view></router-view>
    </navbar-comp>
</template>

<script>

export default{

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
}

/* navbar settings */
nav {
  overflow: hidden;
  position: fixed;
  top: 0;
  width: 100%;
  background-color: #CEDECD;
  box-shadow: #9bc07b 7px 7px 7px;
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
</style>
