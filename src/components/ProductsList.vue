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
                    <img :src="product.image" alt="">
                    <h2>{{ product.name }}</h2>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../assets/scss/partials/variables.scss' as *;

section {
    height: 300px;
    background-color: $section-color;
    padding: 50px 0;

    .products {
        display: flex;
        flex-wrap: wrap;

        .product {
            height: 150px;
            background-color: white;
            width: calc(100% / 4);
            border: 2px solid $main-color;
            text-align: center;
        }
    }
}
</style>