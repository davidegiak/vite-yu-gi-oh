<script>
import MainApp from './components/MainApp.vue'
import cards from './data/cards.js'
export default {
    components:{
        MainApp
    },
    data(){
        return {
            cards
        }
    },
    mounted(){
        axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=50&offset=5").then(function (response) {
        // handle success
        // cards.personaggi = response .data.data.results;
        // console.log(response.data.data)
        cards.dati = response.data.data
        console.log(cards.dati);
  })
    }
}

</script>

<template>
    <MainApp />
</template>
<style scoped>
</style>
