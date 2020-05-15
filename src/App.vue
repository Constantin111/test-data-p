<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/logo.png">
        <HelloWorld msg="Welcome to Your Vue.js App"/>
        <div class="block-produkt">
            <produkt-list @viewDitales="viewDitales"></produkt-list>
            <produkt-details :produkt="selectedProdukt"></produkt-details>
        </div>
    </div>
</template>

<script>
    import HelloWorld from './components/HelloWorld.vue'
    import ProduktList from "./components/ProduktList";
    import ProduktDetails from "./components/ProduktDetails";

    export default {
        name: 'App',
        components: {
            ProduktDetails,
            ProduktList,
            HelloWorld
        },
        data() {
            return {
                selectedProdukt: {}
            }
        },
        methods: {
            viewDitales(produkt){
                this.selectedProdukt = produkt
            }
        }
    }
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }

    .block-produkt {
        display: flex;
        align-items: flex-start;
    }

</style>
