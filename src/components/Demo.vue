<template>
  <div class="hello">
    <h1>Hej! {{id}}</h1>
  </div>
</template>

<script>
export default {
  name: 'Demo',
  props: ['id'],
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>
