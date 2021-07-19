<template>
  
    <div class="container">

        <div class="container--top">

            <img src="@/assets/img/icon-7.png" alt="meet our doctors">

            <h2 class="container--title">tour our facilites</h2>

            <hr class="container--space">

            <p class="container--text">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium <br> doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo <br> inventore veritatis et quasi architecto beatae</p>

            <a href="#"><img src="@/assets/img/play-icon.png" alt=""></a>
           
        </div>

        <div class="container--bottom">
            
            <div class="container--bottom--box background-1">
              
                <h2 class="container--bottom--box--title">Emergency Care</h2>
        
                <img class="container--bottom--box--image" src="@/assets/img/wave-divider.png" alt="wave-divider">
        
                <p class="container--bottom--box--text" >Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque</p>
        
                <button class="container--bottom--box--btn1" >learn more</button>
           
            </div>
           
            <div class="container--bottom--box background-2">
              
                <h2 class="container--bottom--box--title">Emergency Care</h2>
        
                <img class="container--bottom--box--image" src="@/assets/img/wave-divider.png" alt="wave-divider">
        
                <p class="container--bottom--box--text" >Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque</p>
        
                <button class="container--bottom--box--btn2" >learn more</button>
           
            </div>
           
            <div class="container--bottom--box background-3">
              
                <h2 class="container--bottom--box--title">Emergency Care</h2>
        
                <img class="container--bottom--box--image" src="@/assets/img/wave-divider.png" alt="wave-divider">
        
                <p class="container--bottom--box--text" >Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque</p>
        
                <button class="container--bottom--box--btn3" >learn more</button>
           
            </div>
       
        </div>

    </div>

</template>


<script>               

    export default {
        
        name: 'Section4'

    }

</script>


<style scoped lang="scss">

    @import '@/style/variabili.scss';
    @import '@/style/mixins.scss';


    .container {

        .container--top {
            background-image: url("../assets/img/paralax-bg-tour-facilities.jpg");
            @include containerSectionTop-general($Raven, 100%);
            @include backgroundImg ();
            height: 700px;
        }

        .container--bottom {
            height: 400px;
            display: flex;

            .background-1 {
                background-color: $Pelorous;
            }

            .background-2 {
                background-color: $pelorousVibrant;
            }

            .background-3 {
                background-color: $Pelorous2;
            }

            .container--bottom--box {
                text-align: center;
                width: calc(100% / 3);
                padding: 60px;
                color: $White;

                .container--bottom--box--title {
                    font-weight: 300;
                }

                .container--bottom--box--image {
                    margin: 20px 0px;
                }

                .container--bottom--box--text {
                    line-height:2.5;
                    font-size: 15px;
                    font-weight: 300;
                }

                .container--bottom--box--btn1 {
                    @include btnTrasp($Pelorous);
                }

                .container--bottom--box--btn2 {
                    @include btnTrasp($pelorousVibrant);
                }

                .container--bottom--box--btn3 {
                    @include btnTrasp($Pelorous2);
    
                }
    
            }
    
        }

    }

</style>
