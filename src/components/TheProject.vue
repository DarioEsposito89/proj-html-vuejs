<!-- SCRIPT -->
<script>

export default{
    // NAME
    name: "TheProject",

    data(){
        return{
            // ARRAY IMG CARDS
            cardsList:[
                {
                    src: "DRY-1-790x592.jpg",
                    mouse: false
                },

                {
                    src: "221bf0b7-8134-43bb-936a-5acbe42db64a-790x592.jpg",
                    mouse: false
                },

                {
                    src: "z1el4c4p-790x592.jpg",
                    mouse: false
                }
            ]
        }
    },

    methods:{

        // FUNCTION POSITION RIGHT
        getImgsPositionRight: function(){
            const result = new Array(3);

            for (let i = this.cardsList.length - 1; i > -1; i--){
                if (i === 0){
                    result[result.length - 1] = this.cardsList[i];
                }else {
                    result[i - 1] = this.cardsList[i];
                }
            }

            this.cardsList = result;
        },

        // FUNCTION POSITION LEFT
        getImgsPositionLeft: function(){
            const result = new Array(3);

            for (let i = 0; i < this.cardsList.length; i++){
                if(i === this.cardsList.length - 1){
                    result[0] = this.cardsList[this.cardsList.length - 1];
                }else {
                    result[i + 1] = this.cardsList[i];
                }
            }
            
            this.cardsList = result;
        },

        // CHANGE MOUSE
        changeMouse: function(item){
            item.mouse = true;
        },

        // DELETE MOUSE
        deleteMouse: function(item){
            item.mouse = false;
        },

        // IMAGES PATH
        getImgsPath: function(url){
            return new URL(url, import.meta.url).href
        }
    }
}
</script>

<!-- TEMPLATE -->
<template>
    <section id="projects">

        <!-- PROJECT -->
        <div class="project">
            <div class="row gx-0 d-flex justify-content-between align-items-center">

                <!-- TITLE -->
                <div class="title-project col-6 ms-5">
                    <div class="container-subtitle d-flex align-items-center gap-2">
                        <div class="line-green"></div>
                        <h2>PROJECT</h2>
                    </div>
                    <h3>OUR EXPERT TRUSTED CONSULTANTS HELP CLIENTS</h3>
                </div>

                <!-- MOVE SLIDER -->
                <div class="move-slider col-2 text-white">
                    <ul class=" d-flex gap-4 align-items-center">
                        <li @click="getImgsPositionLeft" class="rounded-circle"><i class="fa-solid fa-arrow-left-long"></i></li>
                        <li @click="getImgsPositionRight" class="rounded-circle"><i class="fa-solid fa-arrow-right"></i></li>
                    </ul>
                </div>
            </div>

            <!-- SLIDER -->
            <div class="slider d-flex gap-5 justify-content-center mx-5">

                <!-- CARDS -->
                <div class="card" v-for="(item, index) in cardsList" @mouseenter="changeMouse(item)" @mouseleave="deleteMouse(item)">
                    <img :src="getImgsPath(`../assets/images/${item.src}`)" alt="">

                    <!-- CARD TEXT -->
                    <div class="card-text" :class="!item.mouse ? 'none': ''">
                        <div class="text">
                            <h3>Purinky Products</h3>
                            <p>uncategorized</p>
                        </div>
                        <a href=""><i class="fa-solid fa-plus"></i></a>
                    </div>
                </div>
            </div> 
        </div>
    </section>
</template>

<!-- STYLE -->
<style lang ="scss" scoped>
@use '../styles/partials/variables' as *;

// TITLE
.title-project{
    margin-top: 200px;
    margin-bottom: 30px;
}

    h2{
        color: $text;
        font-size: 16px;
        font-weight: 400px;
        line-height: 25px;
    }

            
        h3{
            font-family: 'Bai Jamjuree', sans-serif;
            padding: 1.5rem 0;
            color: $text;
            font-size: 3rem;
        }

        ul{
            margin-top: 125px;
        }

            li{
                background-color: rgb(15, 15, 15);
                padding: 1rem;
            }

                li:hover{
                    background-color: #39ffbf;
                }

        i{
            cursor: pointer;
            transition-duration: .5s;
            font-size: 30px;
        }

        // SLIDER
        .slider{
        display: flex;
        justify-content: space-between;
        margin-top: 2rem;
        
        // CARDS
        .card{
            position: relative;
            transition-duration: 1s;

            img{
                width: 440px;
            }

            .card-text{
                display: flex;
                justify-content: space-between;
                position: absolute;
                height: 100%;
                width: 100%;
                background-color: rgb(180, 0, 0, .65);
                align-items: end;
                padding-left: 1rem;
                padding-bottom: 1rem;
                
                a{
                    display: inline;
                    width: 30px;
                    height: 30px;
                    background-color: #1f1e38;
                    color: white;
                    margin-right: 1rem;
                    line-height: 30px;
                    text-align: center;
                }

                
                p{
                    color: $paragraph;
                }
            }

            .card-text.none{
                visibility: hidden;
            }
        }
    }
</style>
