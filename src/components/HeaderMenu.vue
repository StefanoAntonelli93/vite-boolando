<script>
export default {
    name: 'HeaderMenu',
};
</script>

<template>
    <nav>
        <ul>menu
            <li><a href="" class="active">li</a></li>
            <li><a href="">li</a></li>
            <li><a href="">li</a></li>
            <li><a href="">li</a></li>
            <li><a href="">li</a></li>
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
        background-color: antiquewhite;
        color: $text-color;

        &.active {
            background-color: $main-color;
        }
    }
}
</style>
