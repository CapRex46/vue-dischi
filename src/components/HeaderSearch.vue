<template>
    <div>
        <nav>
            <select v-model="selected">
                <option v-for="album in albumlist" :key="album.genre"></option>
            </select>
        </nav>
    </div>
</template>

<script>
export default {
    props:{
    rops: {
        albumlist: Object
    }
    },
    data() {
        return {
            selected: "",
            albumlist: []       
            };
    }
}
</script>