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
                    <p class="brand">{{ product.brand }}</p>
                    <p class="name">{{ product.name }}</p>
                    <p class="price">{{ product.price }} &euro;</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../assets/scss/partials/variables.scss' as *;

section {
    background-color: $section-color;
    padding: 50px 0 20px 0;

    .products {
        display: flex;
        flex-wrap: wrap;

        .product {
            background-color: white;
            width: calc(100% / 3);
            border: 5px solid $border-color;
            margin-bottom: 30px;

            img {
                max-width: 100%;
                background-repeat: no-repeat;
                background-size: cover;
            }

            .brand {
                color: gray;
            }

            .price {
                color: red;
                font-weight: 700;
            }

            .name {
                font-weight: 700;
                font-size: large;
                text-transform: uppercase;
            }
        }
    }
}
</style>