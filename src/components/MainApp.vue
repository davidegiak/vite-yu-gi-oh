<script>
import CardList from "./CardList.vue";
export default {
    name:"MainApp",
    components: {
        CardList
    },
    data() {
        return{
        }
    },

}
</script>

<template>
    <main>
        <CardList/>
    </main>
</template>

<style>
main {
    background-color: orange;
    padding-top: 5rem;
}
</style>