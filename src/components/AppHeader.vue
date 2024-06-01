<script>
import AppLogo from './AppLogo.vue';
import HeaderMenu from './HeaderMenu.vue';

export default {
    name: 'AppHeader',
    components: {
        AppLogo,
        HeaderMenu,
    },
};
</script>

<template>
    <header>
        <div class="container">
            <AppLogo />
            <HeaderMenu />
        </div>
    </header>
</template>

<!-- con scoped questi stili vivono solo all'interno di AppHeader -->
<style scoped>
.container {
    text-align: center;
    display: block;
}
</style>
