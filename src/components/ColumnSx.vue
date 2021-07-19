<template>

  <div class="container">
    <div class="container--box">
        <img class="container--image" src="@/assets/img/medical_logo_1x_dark.png" alt="">

        <p class="container--text">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium dolemue launti totam aperiam, eaque ipsa quae abillo. Invente veriatis et quasi architecto beatae luptatem accusantium, remaperiamsiat. Voluptatem accusest etsium doloremque laudaien. Lorem ipsum sits dolores ets unser.</p>

        <h3 class="container--title">learn more about us</h3>

        <i class="social social-face fab fa-facebook-square"></i>
        <i class="social social-twit fab fa-twitter-square"></i>
        <i class="social social-insta fab fa-instagram-square"></i>      
        <i class="social social-yout fab fa-youtube-square"></i>             
    </div>
  </div>

</template>



<script>

export default {

    name: 'ColumnSx'

}

</script>



<style scoped lang="scss">

    @import '@/style/variabili.scss';
    @import '@/style/mixins.scss';

    .container {
        width: calc(100% / 3);
        padding: 20px;
        
        .container--text {
            margin: 20px 0px;
            line-height: 2;
            font-weight: 100;
        }

        .container--title {
            text-transform: uppercase;
            margin: 10px 0px;
            font-weight: 100;
        }

        .social {
            font-size: 40px;
            margin-right: 9px;
        }

        .social-face {
            color: #4267B2;
        }

        .social-twit {
            color: #1DA1F2;;
        }

        .social-insta {
            color: #3f729b;
        }

        .social-yout {
            color: #FF0000;
        }



    }



</style>