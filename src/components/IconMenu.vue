<script>
export default {
    name: "IconMenu",
}
</script>

ScriptCompileContext

<template>
    <ul>
        <li><a href=""><i class="fa-solid fa-user"></i></a></li>
        <li><a href=""><i class="fa-regular fa-heart"></i></a></li>
        <li><a href=""><i class="fa-solid fa-bag-shopping"></i></a></li>
    </ul>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables.scss' as *;

ul {
    display: flex;
    color: $text-header-color;
    gap: 10px;
}

i {
    color: $text-header-color;
}
</style>