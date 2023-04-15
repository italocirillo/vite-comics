<script>
export default {
    name: "Card",
    props: {
        img: String,
        title: String,
    }
}
</script>

<template>
    <div class="card">
        <div class="cornice">
            <img :src="img" :alt="title">
        </div>
        <h4>{{ title }}</h4>
    </div>
</template>

<style lang="scss" scoped>
.card {
    width: calc(100%/6);
    padding: 0.5em;

    .cornice {
        width: calc(80vw /6 - 0.5em);
        height: calc(80vw / 6 - 0.5em);

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top center;
        }
    }


    h4 {
        color: white;
        text-transform: uppercase;
        font-size: 0.8rem;
        font-weight: 200;
        padding: 0.5em 0em;
    }
}
</style>