<script>
import cards from '../data/cards.js'
import Card from './Card.vue'
export default {
    name:"CardList",
    components:{
        Card
    },
    data() {
        return{
            cards
        }
    },
}
</script>

<template>
    <div class="myContainer d-flex gap-3 flex-wrap justify-content-center bg-white p-5">
        <Card v-for="element in cards.dati" :card="element" />
    </div>
</template>