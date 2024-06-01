<script>
import prodotti from '../data/boolando.json';

export default {
    name: 'ProductsList',
    data() {
        return prodotti
    },
    created() {
        console.log(this.products);
    },
};
</script>

<template>
    <section>
        <div class="container">
            <div class="products">
                <div class="product" v-for="(product, index) in products" :key="index">
                    <!-- public + interpolazione per prendere le immagini dal file json -->
                    <img :src="`/images/${product.frontImage}`" alt="">
                    <h4>{{ product.brand }}</h4>
                    <h2>{{ product.name }}</h2>
                    <h3>{{ product.price }} &euro;</h3>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../assets/scss/partials/variables.scss' as *;

section {
    background-color: $section-color;
    padding: 50px 0;

    .products {
        display: flex;
        flex-wrap: wrap;

        .product {
            background-color: white;
            width: calc(100% / 3);
            border: 5px solid $border-color;

            img {
                max-width: 100%;
                background-repeat: no-repeat;
                background-size: cover;
            }
        }
    }
}
</style>