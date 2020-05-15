<template>
    <div class="df-wrap produkt-details">
        <div class="produkt-details__item">
            <div class="namber">Номер продукта - {{produkt.id}}</div>
            <div class="id">id продукта - {{produkt.id}}</div>
            <h4>{{produkt.title}}</h4>
            <div class="price">Цена - {{produkt.price}}</div>
            <div class="qt">Количество - {{produkt.qt}}</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "ProduktDetails",
        props: {
            produkt: {
                type: Object,
                recuired: true
            }
        }
    }
</script>

<style scoped>
    .produkt-details {
        width: 30%;
        border: 1px solid #ccc;
        -webkit-border-radius: 5px;
        -moz-border-radius: 5px;
        border-radius: 5px;
        min-height: 50px;
        padding: 15px;
    }
    .produkt-details__item {
        text-align: left;
        border: 1px solid #ccc;
        -webkit-border-radius: 5px;
        -moz-border-radius: 5px;
        border-radius: 5px;
        padding: 15px;
    }
</style>