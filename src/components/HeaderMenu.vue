<script>
export default {
    name: 'HeaderMenu',
};
</script>

<template>
    <nav>
        <ul>
            <li><a href="" class="active">Donna</a></li>
            <li><a href="">Uomo</a></li>
            <li><a href="">Bambini</a></li>
        </ul>
    </nav>
</template>


<style scoped lang="scss">
@use '../assets/scss/partials/variables.scss' as *;

/* metodo nesting */
ul {
    display: flex;
    justify-content: center;

    a {
        display: inline-block;
        padding: 20px 10px;
        color: $text-header-color;

        &.active {
            background-color: $active-color;
        }
    }
}
</style>
