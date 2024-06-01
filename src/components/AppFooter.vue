<script>

export default {
    name: 'AppFooter',
};  
</script>


<template>
    <footer>
        <div class="container">
            <div>
                <p>title</p>
                <p>testoooooooooooooooooooooo

                </p>
            </div>
            <div>
                <ul>
                    <li>icona</li>
                    <li>icona</li>
                    <li>icona</li>
                    <li>icona</li>
                    <li>icona</li>
                </ul>
            </div>
        </div>
    </footer>
</template>


<style scoped lang="scss">
@use '../assets/scss/partials/variables.scss' as *;

footer {
    background-color: $footer-color;

    .container {
        display: flex;
        color: $text-footer-color;
        justify-content: space-between;

    }
}
</style>
