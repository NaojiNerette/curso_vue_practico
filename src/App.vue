<script>
import Test from "./components/Test";
import User from "./components/User.vue";

export default {
  name: 'App',
  components: {
    Test,
    User
  }
}
</script>


<template>
  <div id="app">
    <h1>Hola mundo!</h1>
    <!--<Test msg="HOLA DESDE EL PADRE"/>-->
    <User />
  </div>
</template>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
