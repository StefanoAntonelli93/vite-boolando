<script>
// importo componenti che formano header
import AppLogo from './AppLogo.vue';
import HeaderMenu from './HeaderMenu.vue';
import IconMenu from './IconMenu.vue';

export default {
    name: 'AppHeader',
    components: {
        AppLogo,
        HeaderMenu,
        IconMenu,
    },
};
</script>

<template>
    <header>
        <div class="container">
            <HeaderMenu />
            <AppLogo />
            <IconMenu />
        </div>
    </header>
</template>

<!-- con scoped questi stili vivono solo all'interno di AppHeader -->
<style scoped lang="scss">
// richiamo variables.scss
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
