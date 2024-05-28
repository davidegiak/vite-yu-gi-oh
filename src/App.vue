<script>
import MainApp from './components/MainApp.vue'
import cards from './data/cards.js'
import HeaderApp from './components/HeaderApp.vue'
export default {
    components:{
        MainApp,
        HeaderApp
    },
    data(){
        return {
            cards,
        }
    },
    methods: {
        selecta(x) {
            axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=`${x}`&num=100&offset=0").then((r)=> {
                this.cards.dati = r.data.data
            })
        }
    },
    mounted(){
        axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=100&offset=0").then((response)=> {
        this.cards.dati = response.data.data
        console.log(cards);

        // for (const card of this.cards.dati) {
        //     if (!this.cards.archetipo.includes(card.archetype)) {
        //         this.cards.archetipo.push(card.archetype)
        //     }
        // }
        // console.log(this.cards.archetipo)
    })
    axios.get("https://db.ygoprodeck.com/api/v7/archetypes.php").then((r)=> {
        this.cards.archetipo = r.data
        console.log(cards.archetipo);
  })
    }
}

</script>

<template>
    <HeaderApp />
    <div class="myContainer">
        <select name="select" id="select">
            <option v-for="archetype in cards.archetipo" value=""> {{ archetype.archetype_name }} </option>
        </select>
    </div>
    <MainApp />
</template>
<style scoped>
.myContainer {
    display: flex;
    align-items: end;
    transform: translateY(5rem);
}
</style>
