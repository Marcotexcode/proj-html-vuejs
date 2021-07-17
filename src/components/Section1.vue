<template>
  
    <div class="container">

        <h2 class="container--title">Welcome to Avada Health</h2>

        <p class="container--text">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium <br> doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo</p>

        <div class="container--container-box" >

            <div class="container--container-box--box" v-for="(item, index) in items" :key="index">
                
                <img class="container--container-box--box--image" :src="require(`@/assets/img/${item.img}`)" :alt="item.title">
                
                <h3 class="container--container-box--box--title">{{item.title}}</h3>
                
                <p class="container--container-box--box--text">{{item.text}}</p>
            
            </div>

        </div>

    </div>

</template>


<script>               

    import SectionOneItems from '@/data/SectionOneItems.js';

    export default {
        
        name: 'Section1',

        data() {

            return {

                items: SectionOneItems

            }

        }

    }

</script>


<style scoped lang="scss">

    @import '@/style/variabili.scss';
    @import '@/style/mixins.scss';

    .container {
        @include containerCenter-general($Raven);

        @include containerBox(285px);
        
    }

</style>
