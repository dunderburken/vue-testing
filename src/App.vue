<template>
  <div id="app">
    <Menu></Menu>
    <img src="./assets/logo.png">
    <h1>{{$route.params.id}}</h1>
    <div>Menu</div>
    <router-link to="/">Hello Wrold</router-link>
    <router-link to="/demo/666">Demo</router-link>
    <router-link v-bind:key="item" v-for="item in [1,2,3,4]" :to="{path:'/demo/' + item}">Demo {{item}}</router-link>
    <router-link v-bind:key="item" v-for="item in [11,12,13,14]" :to="{name:'Demo', params:{id: item}}">Demo {{item}}</router-link>
    <transition name="fade">
      <router-view/>
    </transition>
  </div>
</template>

<script>
import Menu from './components/Menu'

export default {
  name: 'App',
  components: { Menu },
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
