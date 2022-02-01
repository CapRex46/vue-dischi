<template>
  <div id="app">
    <header-search @filtro1="genfilter"/>
    <main-content :albumlist = "albumfiltergen"/>
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
      albumlist: [] ,
      albumfiltergen: [],
    }   
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response)  => {
      this.albumlist = response.data.response;
      this.albumfiltergen = response.data.response;
    }) 
  },
  methods: {
    genfilter(searchTerm) {
       if (searchTerm === 'All') {
        this.albumfiltergen = this.albumlist;
      } else {
        this.albumfiltergen = this.albumlist.filter((album) => {
          return album.genre.includes(searchTerm);
        });
      }
    }
  }
}
</script>




<style lang="scss">

@import './style/main.scss'

</style>
