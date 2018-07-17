<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld ok="okok bro" msg="Welcome to Your Vue.js App"/>

   </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  data: () => ({message : "ok super ça marche enfin "}),
  methods: {
     copy() {

     },
     hover() {
       this.clicked = false;
     }
   }


}
</script>

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
