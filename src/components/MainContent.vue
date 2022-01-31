<template>
<div>
     <album-box v-for="album in albumlist" 
    :key="album.title"
    :album="album"
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