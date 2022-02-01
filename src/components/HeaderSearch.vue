<template>
    <div>
        <select v-model="ketwordSearch">
            <option $emit('search, ketwordSearch')></option>
        </select>
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
            keywordSearch: "",     
            };
    }
}
</script>