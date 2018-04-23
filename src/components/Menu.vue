<template>
        <nav class="col-md-2 d-none d-md-block bg-light sidebar">
          <div class="sidebar-sticky">

            <ul class="nav flex-column">
              <li class="nav-item">
                <router-link class="nav-link" to="/">Hello Wrold</router-link>
              </li>
              <li class="nav-item">
                <router-link class="nav-link" to="/demo/666">Demo</router-link>
              </li>
              <li v-bind:key="item" v-for="item in [1,2,3,4]" class="nav-item">
                <router-link class="nav-link" v-bind:key="item" :to="{path:'/demo/' + item}">Demo {{item}}</router-link>
              </li>
              <li v-bind:key="item" v-for="item in [11,12,13,14]" class="nav-item">
                <router-link class="nav-link" v-bind:key="item" :to="{name:'Demo', params:{id: item}}">Demo {{item}}</router-link>
              </li>

              <li class="nav-item">
                <a class="nav-link active" href="#">
                  <span data-feather="home"></span>
                  Dashboard <span class="sr-only">(current)</span>
                </a>
              </li>
            </ul>
          </div>
        </nav>
</template>

<script>
export default {
  name: 'Menu',
  data () {
    return {
    }
  }
}
</script>
