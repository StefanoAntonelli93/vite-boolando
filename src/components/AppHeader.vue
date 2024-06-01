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
            <HeaderMenu />
            <AppLogo />
            icon menu
        </div>
    </header>
</template>

<!-- con scoped questi stili vivono solo all'interno di AppHeader -->
<style scoped lang="scss">
@use '../assets/scss/partials/variables.scss' as *;

header {
    background-color: $header-color;

}

.container {
    text-align: center;
    display: flex;
    justify-content: space-around;
    align-items: center;
}
</style>
