<template>
  
    <div class="container">

        <img class="container--image" src="@/assets/img/medical_logo_1x_light.png" alt="">

        <ul class="container--menu">
            
            <li class="container--menu--list" v-for="(link, index) in links" :key="index">
                
                <a class="container--menu--list--items"  :class="link.type == true ? 'active' : ' ' " :href="link.url">{{link.text}}</a>
           
            </li>

            <li class="container--menu--list">

                <a class="container--list--btn" href="#">make appointment</a>

            </li>

        </ul>

    </div>

</template>


<script>               

        import MenuItems from '@/data/MenuItems.js';


    export default {
        
        name: 'Header',

        data() {

            return {

                links: MenuItems

            }

        }

    }

</script>


<style scoped lang="scss">

    @import '@/style/variabili.scss';
    @import '@/style/mixins.scss';

    .container {
       padding: 20px;
       display: flex;
       align-items: center;
       justify-content: space-between;

       .container--image {
           width: 200px;
       }

       .container--menu {
           display: flex;

           .container--menu--list {
               margin: 0px 10px;
               list-style: none;

                .container--menu--list--items {
                    color: #ffffff;
                    text-decoration: none;
                    text-transform: uppercase;
                }

            }

            .container--list--btn {

                @include btnPelorous();
                    
            }

        }

    }



</style>
