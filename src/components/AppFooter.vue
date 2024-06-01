<script>

export default {
    name: 'AppFooter',
};  
</script>


<template>
    <footer>
        <div class="container">
            <div>
                <p class="title">Boolando srl</p>
                <ul>
                    <li><a href="">Informazioni legali</a></li>
                    <li><a href="">Informativa sulla privacy</a></li>
                    <li><a href="">Diritti di recesso</a></li>
                </ul>
            </div>
            <div>
                <p>Trovaci anche su</p>
                <ul>
                    <li><a href=""><i class="fa-brands fa-square-twitter"></i></a></li>
                    <li><a href=""><i class="fa-brands fa-square-facebook"></i></a></li>
                    <li><a href=""><i class="fa-brands fa-square-instagram"></i></a></li>
                    <li><a href=""><i class="fa-brands fa-square-pinterest"></i></a></li>
                    <li><a href=""><i class="fa-brands fa-square-youtube"></i></a></li>
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
        padding: 30px 0;

        .title {
            font-weight: 700;
            font-size: 20px;
        }

        ul {
            display: flex;
            justify-content: space-between;
            padding-top: 10px;
            gap: 15px;


            a {
                color: $text-footer-color;

                i {
                    font-size: 20px;
                }

            }
        }

    }
}
</style>
