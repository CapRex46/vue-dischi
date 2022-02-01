<template>
  <div id="app">
    <header-search @search="searchGenre"/>
    <main-content :albumlist = "albumlist"/>
  </div>
</template>

<script>
import axios from 'axios'
import MainContent from './components/MainContent.vue'
import HeaderSearch from './components/HeaderSearch.vue'


export default {
  name: 'App',
  components: {
    MainContent,
    HeaderSearch,
  },
  data () {
    return {
      albumlist: [] 
    }   
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response)  => {
      this.albumlist = response.data.response
    }) 
  },
  methods: {
    searchGenre(keyword) {
      alert(keyword)
    }
  }
};
</script>




<style lang="scss">

@import './style/main.scss'

</style>
