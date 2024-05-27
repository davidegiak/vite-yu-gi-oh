<script>
export default {
    name: "Card",
    props:{
        card: String
    },
    data() {
    }
}
</script>

<template>
    <div class="myCard d-flex flex-column gap-3 text-center">
        <div class="img-cont">
            <img :src="card.card_images[0].image_url" alt="">
        </div>
        <h5> {{ card.name }} </h5>
        <p> {{ card.archetype }} </p>
    </div>
</template>

<style>
.myCard{
    width: calc(100% / 5 - 1rem);
    background-color: orange;
}

.img-cont {
    width: 100%;
}
img {
    width: 100%;
}
</style>