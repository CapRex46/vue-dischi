<template>
  <div id="app">
    
  </div>
</template>

<script>
import axios from 'axios'
import AlbumBox from './components/AlbumBox.vue'


export default {
  name: 'App',
  components: {
    MainContent,
    AlbumBox,
  },
  data () {
    return {
      album: [] 
    }
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response)  => {
      this.personaggi = response.data
    }) 
  }
}
</script>




<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

@import './style/main.scss'

</style>
