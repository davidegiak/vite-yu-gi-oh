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

        }
    }
}
</script>

<template>
    <Card v-for="element in cards.dati" :card="dati.card_immages"/>
</template>