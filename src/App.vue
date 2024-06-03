<!-- js -->
<script>
// importo componenti su app principale
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import ProductsList from './components/ProductsList.vue';

export default {
    name: 'MyApp',
    components: {
        AppHeader,
        AppFooter,
        ProductsList,
    },
};
</script>

<!-- html -->
<template>
    <AppHeader />
    <main>
        <ProductsList />
    </main>
    <AppFooter />
</template>


<!-- css -->
<!-- con lang si può creare css anche su app principale -->
<style lang="scss" scoped>
// importo qui con @use il main.scss </style>
