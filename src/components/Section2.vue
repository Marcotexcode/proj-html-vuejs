<template>

    <div class="conteiner-general">

        <div class="container">

            <img src="@/assets/img/icon-5.png" alt="meet our doctors">

            <h2 class="container--title">meet our doctors</h2>

            <hr class="container--space">

            <p class="container--text" >Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium <br> doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo <br> inventore veritatis et quasi architecto beatae</p>

            <div class="container--container-box">

                <div class="container--container-box--box" v-for="(item, index) in items" :key="index">

                    <div class="image-container">
                        
                        <img class="container--container-box--box--image" :src="require(`@/assets/img/${item.img}`)" :alt="item.title">

                    </div>   
                    
                    <div class="item-container">

                        <h3 class="container--container-box--box--title">{{item.title}}</h3>

                        <span>{{item.subtitle}}</span>

                        <p class="container--container-box--box--text">{{item.text}}</p>

                        <i class="social social-face" :class="item.facebook"></i>
                        <i class="social social-twit" :class="item.twitter"></i>
                        <i class="social social-insta" :class="item.instagram"></i>

                    </div>
                    
                </div>

            </div>

        </div>

    </div>

</template>


<script>               

    import SectionTwoItems from '@/data/SectionTwoItems.js';

    export default {

        name: 'Section2',

        data() {

            return {

                items: SectionTwoItems

            }

        }

    }

</script>


<style scoped lang="scss">

    @import '@/style/variabili.scss';
    @import '@/style/mixins.scss';


    .conteiner-general {
        background-color: $Gallery;

        .container {
            @include containerCenter-general($Raven);

            .container--title {
                text-transform: uppercase;
                margin: 20px 0px;
            }

            .container--space {
                width: 30%;
                margin: 35px auto;
                border: 1px solid $FrenchGray;  
            }

            .container--container-box {
                width: 90%;
                margin: 0 auto;
                display: flex;
                justify-content: space-between;
                flex-wrap: wrap;
                margin-top: 90px;
                text-align: left;

                .container--container-box--box {
                    width: 300px;
                    background-color: #fff;

                    .container--container-box--box--image {
                        width: 100%;                                       
                    }

                    .container--container-box--box--image:hover {
                        transition: 0.5s ease-out;
                        transform: scale(1.1);
                        box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;

                    }

                    .item-container {
                        padding: 20px;

                        .container--container-box--box--title {
                            margin: 20px 0px;
                            text-transform: uppercase;
                            font-size: 18px;
                        }

                        .container--container-box--box--text {
                            line-height: 2.5;
                            font-size: 13.5px;
                        }

                        .social {
                            font-size: 35px;
                            margin-right: 10px;
                        }

                        .social-face {
                            color: #3c5998;
                        }

                        .social-twit {
                            color: #54acee;
                        }

                        .social-insta {
                            color: #3f729b;
                        }

                    }

                }

            }
            
        }

    }

</style>
