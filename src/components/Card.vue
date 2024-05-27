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
    <img :src="card.image_url" alt="">
</template>