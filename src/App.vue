<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>{{$route.params.id}}</h1>
    <div>Menu</div>
    <router-link to="/">Hello Wrold</router-link>
    <router-link v-bind:key="item" v-for="item in [1,2,3,4]" to="{path:'/demo/id' + item}">Demo</router-link>
    <transition name="fade">
      <router-view/>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'App'
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
