<template>
<div>
     <album-box v-for="albumlist in album" 
    :key="albumlist.title"
    /> 
</div>

</template>


<script>
import AlbumBox from './AlbumBox.vue'

export default {
    components: {
        AlbumBox
    },
    props: {
        albumlist: Array
    }
}
</script>


<style lang="scss" scoped>
    
</style>