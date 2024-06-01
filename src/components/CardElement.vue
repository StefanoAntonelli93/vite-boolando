<script>
export default {
    name: 'CardElement',
    props: ['image', 'brand', 'name', 'price'],
}
</script>


<template>
    <div class="product">
        <img :src="image" :alt="brand">
        <p class="brand">{{ brand }}</p>
        <p class="name">{{ name }}</p>
        <p class="price">{{ price }} &euro;</p>
    </div>
</template>
