<template>
    <div class="df-wrap produkt-item">
        <div class="num-produkt">Номер продукта - {{index}}</div>
        <div class="id-produkt">id - {{produkt.id}}</div>
        <h3 class="name-produkt">{{produkt.title}}</h3>
        <div class="price-rpodukt">Стоимость - {{produkt.price}}</div>
        <div class="qt-produkt">qt - {{produkt.qt}}</div>
        <div class="wue-ditales" @click="viewDitalesCklied">Посмотреть детали</div>
    </div>
</template>

<script>
    export default {
        name: "ProduktItem",
        props: {
            produkt: {
                type: Object,
                recuired: true
            },
            index: [Number, String]
        },
        methods: {
            viewDitalesCklied() {
                this.$emit("viewDitales", this.produkt.id)
            }
        }
    }
</script>

<style scoped>
    .produkt-item {
        text-align: left;
        padding: 20px;
        margin-bottom: 20px;
        border: 1px solid #ccc;
        -webkit-border-radius: 5px;
        -moz-border-radius: 5px;
        border-radius: 5px;
        min-height: 50px;
    }

    .wue-ditales {
        display: inline-flex;
        padding: 15px;
        color: #fff;
        background: blue;
        margin-top: 15px;
        cursor: pointer;
        -webkit-border-radius: 5px;
        -moz-border-radius: 5px;
        border-radius: 5px;
    }
</style>