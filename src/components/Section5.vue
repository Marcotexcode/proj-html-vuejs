<template>
  
    <div class="container">

       <div class="container--top">

            <h2 class="container--title">Make An Appointment</h2>

            <hr class="container--space">

            <p class="container--text">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium <br> doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo <br> inventore veritatis et quasi architecto beatae</p>

            <form class="container-form" action="">

                <input class="container-form--input1" placeholder="Name*">
                <input class="container-form--input1" placeholder="Email*">
                <input class="container-form--input1" placeholder="Phone Number*">
                <input class="container-form--input1" placeholder="Appointment Date*">
                <input class="container-form--input2" placeholder="How can we help?*">

                <button class="container-form--btn">make an appointment</button>

            </form>
           
        </div>

        <div class="container-slider">

            <VueSlickCarousel v-bind="settings" class="container-box--element">

                <div  class="element" v-for="(item,index) in items"  :key="index" >

                    <img  class="element--image" :src="require(`@/assets/img/${item.img}`)" alt="">

                </div>  

            </VueSlickCarousel>

        </div>

    </div>

</template>


<script>               

    import SectionFive from '@/data/SectionFive.js';
    import VueSlickCarousel from 'vue-slick-carousel'
    import 'vue-slick-carousel/dist/vue-slick-carousel.css'

    export default {
        
        name: 'Section5',

        components: { 

            VueSlickCarousel 

            },
            
        data() {

            
            return {

                settings: {

                    "arrows": false,
                    "dots": false,
                    "infinite": true,
                    "slidesToShow": 3,
                    "slidesToScroll": 1,
                    "autoplay": true,
                    "speed": 3000,
                    "autoplaySpeed": 2000,
                    "cssEase": "linear"

                },

                items: SectionFive

            }

        },
    
    }

</script>


<style scoped lang="scss">

    @import '@/style/variabili.scss';
    @import '@/style/mixins.scss';

    .container {

        .container--top {
            
            background-image: url("../assets/img/make-an-appointment.jpg");
            
            @include containerSectionTop-general($Raven, 100%);
            
            @include backgroundImg ();
            


            .container-form {
                width: 50%;
                margin: 0 auto;
                
                .container-form--input1 {
                    color: $White;
                    padding: 10px;
                    border: 1px solid $White;
                    background-color: rgba(255, 255, 255, 0);
                    width: calc(100% / 2 - 20px);
                    height: 40px;
                    margin: 10px 10px;
                }

                .container-form--input2 {
                    color: $White;
                    padding: 10px;
                    border: 1px solid $White;
                    background-color: rgba(255, 255, 255, 0);
                    width: calc(100% - 20px);
                    height: 100px;
                    margin: 10px 10px;
                }

                .container-form--btn {
                    height: 50px;
                    width: calc(100% - 20px);
                    text-transform: uppercase;
                    font-size: 18px;
                    color: $White;
                    border-radius: 2px;
                    background-color:$Pelorous;
                    border: none;

                    &:hover {
                    background-color:$Pelorous2;

                    }

                }

            }
       
        }

        .container-slider {
            background: rgb(57,175,187);
            background: linear-gradient(90deg, rgba(57,175,187,1) 14%, rgba(59,155,189,1) 41%, rgba(68,149,191,1) 52%, rgba(68,139,191,1) 69%);
            padding: 50px;
            
            .container-box--element {
                width: 80%;
                margin: 0 auto;
                display: flex;
                justify-content: center;
                overflow:hidden;

                .element--image {
                    width: 250px;
                    margin-left: 100px;
                }

            }
            
        }

    }

</style>
