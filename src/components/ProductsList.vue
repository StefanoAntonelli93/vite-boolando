<script>
// importo file json in lista prodotti 
import prodotti from '../data/boolando.json';
// importo componente CardElement in ProductList
import CardElement from './CardElement.vue';

export default {
    name: 'ProductsList',
    components: {
        CardElement,
    },
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
                <!-- proprietà padre ereditato da primo figlio e SOLO primo figlio -->
                <!-- ciclo v-for per iterare ogni oggetto della lista -->
                <!-- creo link per props in CardElement -->
                <CardElement v-for="(product, index) in products" :key="index" :image="`/images/${product.frontImage}`"
                    :brand="product.brand" :name="product.name" :price="product.price" />
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
// uso variables.scss
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

            :deep(img) {
                max-width: 100%;
                background-repeat: no-repeat;
                background-size: cover;
            }

            :deep(.brand) {
                color: gray;
            }

            :deep(.price) {
                color: red;
                font-weight: 700;
            }

            :deep(.name) {
                font-weight: 700;
                font-size: large;
                text-transform: uppercase;
            }
        }
    }
}
</style>