<script>
import CardList from "./CardList.vue"
export default {
    name:"MainApp",
    components: {
        CardList
    },
    data() {
        return{
        }
    },
//     created() {
//     axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0").then(risultato => {
//       this.cards.data = risultato.data.results;
//     });
//   },

}
</script>

<template>
    <CardList/>
</template>