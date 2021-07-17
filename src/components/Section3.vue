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

        @include containerSectionTop-general($Raven);

        .container--container-box {
            width: 90%;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-top: 90px;

            .container--container-box--box {
                width: 350px;
                margin: 20px 0px;

                .container--container-box--box--title {
                    margin: 20px 0px;
                    text-transform: uppercase;
                    font-size: 18px;
                }

                .container--container-box--box--text {
                    line-height: 2.5;
                    font-size: 13.5px;

                }

            }

        }

    }

</style>
