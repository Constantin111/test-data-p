<template>
    <div class="df-wrap produkt-list">
        <div class="df-wrap produkt-item__block">
            <produkt-item v-for="(produkt, i) in produkts"
                          :key="produkt.id"
                          :produkt="produkt"
                          :index="(i+1)"
                          @viewDitales="viewDitales"
            >
            </produkt-item>
        </div>
    </div>
</template>

<script>
    import ProduktItem from "./ProduktItem";
    import _ from 'lodash';

    export default {
        name: "ProduktList",
        components: {ProduktItem},
        data() {
            return {
                produkts: [
                    {
                        id: 1,
                        title: 'Первый продукт',
                        price: 50,
                        qt: 170
                    },
                    {
                        id: 2,
                        title: 'Второй продукт',
                        price: 150,
                        qt: 456
                    },
                    {
                        id: 3,
                        title: 'Третий продукт',
                        price: 250,
                        qt: 1900
                    },
                    {
                        id: 4,
                        title: 'Четвёртый продукт',
                        price: 540,
                        qt: 643
                    },
                    {
                        id: 5,
                        title: 'Пятый продукт',
                        price: 501,
                        qt: 563
                    },
                    {
                        id: 6,
                        title: 'Шестой продукт',
                        price: 150,
                        qt: 565
                    }
                ]
            }
        },
        methods: {
            viewDitales(id) {
                let ProduktToVuew = _.find(this.produkts, {id:id})
                this.$emit("viewDitales", ProduktToVuew)
            }
        }
    }
</script>

<style scoped>
    .produkt-list {
        width: 70%;
        padding-right: 30px;
    }

    .produkt-item__block {
        width: 100%;
        padding: 20px;
        border: 1px solid #ccc;
        -webkit-border-radius: 5px;
        -moz-border-radius: 5px;
        border-radius: 5px;
        min-height: 50px;
    }
</style>