<script>
import cards from '../data/cards.js'
import Card from './Card.vue'
export default {
    name:"CardList",
    props:{

    },
    data() {
        return{

        }
    }
}
</script>

<template>
    <Card v-for="element in cards" :card="dati.card_immages"/>
</template>