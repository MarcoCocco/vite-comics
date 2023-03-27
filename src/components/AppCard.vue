<script>

export default {
    name: 'AppCard',

    data() {
        return {

        }
    },

    props: {
        thumb: String,
        price: String,
        series: String,
        type: String,
    },
}
</script>

<template>
    <div id="card">
        <img :src="thumb" alt="">
        <div id="series">
            <p>{{ series }}</p>
        </div>
        <div id="type">
            <p>{{ type }}</p>
        </div>
        <div id="price">
            <p>{{ price }}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
#card {
    width: calc(100% / 6 - 20px);
    display: flex;
    flex-direction: column;
    font-size: .8em;

    #series {
        font-weight: bold;
        font-size: 1.2em;
    }

    img {
        height: 200px;
        object-fit: cover;
        object-position: top;
    }

}
</style>