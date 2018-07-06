<template>
  <div id="app">
    
    
    <v-start></v-start>
    <router-view></router-view>
  </div>
</template>

<script>
import Start from './components/Start.vue';
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components:{
      'v-start':Start
  }
}
</script>

<style lang="scss">

</style>
