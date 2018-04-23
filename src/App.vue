<template>
  <div id="app" class="container">
    <TopMenu></TopMenu>

    <div class="container-fluid">
      <div class="row">
        <Menu></Menu>
        <main role="main" class="col-md-9 ml-sm-auto col-lg-10 px-4">
          <div class="d-flex justify-content-between flex-wrap flex-md-nowrap align-items-center pt-3 pb-2 mb-3 border-bottom">

            <img src="./assets/logo.png">
            <h1>{{$route.params.id}}</h1>
            <div>Menu</div>

            <transition name="fade">
              <router-view/>
            </transition>
            <h1 class="h2">Dashboard</h1>
            <div class="btn-toolbar mb-2 mb-md-0">
              <div class="btn-group mr-2">
                <button class="btn btn-sm btn-outline-secondary">Share</button>
                <button class="btn btn-sm btn-outline-secondary">Export</button>
              </div>
              <button class="btn btn-sm btn-outline-secondary dropdown-toggle">
                <span data-feather="calendar"></span>
                This week
              </button>
            </div>
          </div>

          <canvas class="my-4 w-100" id="myChart" width="900" height="380"></canvas>

        </main>
      </div>
    </div>
  </div>
</template>

<script>
import Menu from './components/Menu'
import TopMenu from './components/TopMenu'

export default {
  name: 'App',
  components: { Menu, TopMenu }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
  margin-top: 60px;
}
</style>
