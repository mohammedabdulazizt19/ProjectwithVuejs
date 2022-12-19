<template>
  <!--<img alt="Vue logo" src="./assets/logo.png">-->
  <!--<HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div id="app" class="h-100">
    <div class="container-fluid h-100">
      <div class="row h-100">
        <div class="col-12 h-100 d-flex justify-content-center">
          <div class="col-md-8 px-5 py-4 text-left">
            <LogIn />
          </div>
         
        </div>
      </div>

    </div>
    
  </div>

</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import LogIn from './components/LogIn.vue'
export default {
  name: 'App',
  components: {
    LogIn
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
