<template>
  <div id="app">
    <component v-bind:is="Cmp"></component>
    <button v-on:click="updateCmp('signin')">Load SignIn</button>
    <button v-on:click="updateCmp('signup')">Load SignUp</button>
  </div>
</template>

<script>
import SignIn from './components/SignIn.vue'
import SignUp from './components/SignUp.vue'

export default {
  name: 'App',
  components: {
    'signin':SignIn,
    'signup':SignUp
  },
  data(){ 
    return{
      Cmp:'signin',
    }
  },
  methods:{
    updateCmp(item){
      this.Cmp=item
    }
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
