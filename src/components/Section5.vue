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

            <Slider/>   

            <div class="container-box--element">

                <div class="element" v-for="(item,index) in items"  :key="index" >

                    <img class="element--image" :src="require(`@/assets/img/${item.img}`)" :style="{'margin-left': '-' + (100 * contatore) + '%'}" alt="">

                </div>  

            </div>

        </div>

    </div>

</template>


<script>               

    import SectionFive from '@/data/SectionFive.js';

    export default {
        
        name: 'Section5',

        data() {

            
            return {

                contatore: 0,

                items: SectionFive

            }

        },

       
        methods: {
       
            nextAlbun() {
        
                this.contatore++;
        
                if (this.contatore > this.items.lenght - 1){
        
                    this.contatore = 0
        
                } else {
                   
                   this.contatore ++
               
                }
        
                console.log(this.contatore);
        
            }
       
        },

        mounted() {

            setInterval(this.nextAlbun, 3000)
  
        }

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
            background-color:$Pelorous2;
            padding: 50px;
                z-index: 2;
            
            .container-box--element {
                width: 50%;
                border: 1px solid #000;
                margin: 0 auto;
                display: flex;
                justify-content: center;
                z-index: 1;
                // overflow:auto;

                .element--image {
                    width: 250px;
                    margin-right: 30px;
                    
                }

            }
            
        }

    }

</style>
