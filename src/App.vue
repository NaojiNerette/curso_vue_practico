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
    <nav>
      <ul>
        <li>
          <router-link to="/test">Test</router-link>
        </li>
      </ul>
      <ul>
        <li>
          <router-link to="/">User</router-link>
        </li>
      </ul>
    </nav>
    <router-view></router-view>

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
