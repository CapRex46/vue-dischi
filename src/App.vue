<template>
  <div id="app">
    <main-content />
  </div>
</template>

<script>
import axios from 'axios'
import MainContent from './components/MainContent.vue'



export default {
  name: 'App',
  components: {
    MainContent,

  },
  data () {
    return {
      albums: [] 
    }   
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response)  => {
      this.album = response.data
    }) 
  }
}
</script>




<style lang="scss">

@import './style/main.scss'

</style>
