<template>
  
    <div class="container">

        <h2 class="container--title" >Caring <span class="container--title--color-title">For Life</span></h2>

        <p class="container--text">Kind words can be short and easy to speak, but their echoes are truly endless. Avada Health focuses on you as if it was our own family.</p>

        <a class="container--btn" href="#">learn more</a>

    </div>

</template>


<script>               

    export default {
        
        name: 'Jumbotron'

    }

</script>


<style scoped lang="scss">

    @import '@/style/variabili.scss';
    @import '@/style/mixins.scss';

    .container {
        width:50%;
        height:60%;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translateY(-40%) translateX(-50%);
        padding: 20px;

        .container--title {
            font-size: 50px;
            color: $White;
            font-weight: 300;

            .container--title--color-title {
                color: $pelorousVibrant;
            }

        }

        .container--text {
            color: $White;
            margin: 50px 0px;           
        }

        .container--btn {
            @include btnPelorous();                    
        }
        
    }

</style>
