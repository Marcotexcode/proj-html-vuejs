<template>
  
    <div class="container">

        <img src="@/assets/img/icon-6.png" alt="meet our doctors">

        <h2 class="container--title">our health service</h2>

        <hr class="container--space">

        <p class="container--text">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium <br> doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo <br> inventore veritatis et quasi architecto beatae</p>

        <div class="container--container-box">

            <div class="container--container-box--box" v-for="(item, index) in items" :key="index">
                
                <img class="container--container-box--box--image" :src="require(`@/assets/img/${item.img}`)" :alt="item.title">
                
                <h3 class="container--container-box--box--title">{{item.title}}</h3>
                
                <p class="container--container-box--box--text">{{item.text}}</p>
            
            </div>

        </div>

    </div>

</template>


<script>           

    import SectionThreItems from '@/data/SectionThreItems.js';

    export default {
        
        name: 'Section3',

        data() {

            return {

                items: SectionThreItems

            }

        }

    }

</script>


<style scoped lang="scss">

    @import '@/style/variabili.scss';
    @import '@/style/mixins.scss';
        
    .container {

        @include containerSectionTop-general($Raven,90%);

        @include containerBox(350px);

        .container--container-box--box {
            margin: 20px 0px;

        }
        
    }

</style>
