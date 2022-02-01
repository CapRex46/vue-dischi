<template>
    <div>
        <select v-model="selectgen" @change="$emit('filtro1', selectgen)">
                <option value="All">All</option>
                <option value="Jazz">Jazz</option>
                <option value="Metal">Metal</option>
                <option value="Pop">Pop</option>
                <option value="Rock">Rock</option>
        </select>
    </div>
</template>

<script>
export default {
    data() {
        return {
            selectgen: "",     
            };
    }
}
</script>