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
    }
}
</script>

<template>
    <Card v-for="element in cards.dati" />
</template>