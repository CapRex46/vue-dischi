<template>
<div class="albumcontent">
    <div class="albumboxes">
        <div class="albumalign">
            <img :src="album.poster" alt="">
            <div class="albuminfo">
                <p>{{album.title}}</p>
                <p>{{album.author}}</p>
                <p>{{album.year}}</p>
                <p>{{album.genre}}</p>
            </div>

        </div>

    </div>
</div>

</template>


<script>
export default {
    props: {
        album: Object
    }
}
</script>


<style lang="scss" scoped>
    .albumcontent{
        background: #1C1C1C;
        width: 100%;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
    } .albumboxes{
        width: 16%;
        display:flex ;
        background: lightgrey;
        justify-content: center;
        margin: 0 auto;
        margin-top: 20px ;
    }
    .albuminfo {
        color: rgb(20, 20, 20);
        width: 200px;
        font-size: 15px;
        text-align: center;
        margin-top: 20px;
        margin-bottom: 20px;
    } img {
        width: 200px;
        padding: 20px;
    } .albumaling {
        width: 900px;
    }
</style>