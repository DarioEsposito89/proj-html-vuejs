<script>
import { store } from '/store.js'

export default {
    name: "TheHeader",
    components: {
        store,
    },
    data() {
        return {
            navigationLinks: [

                {
                    voice: "HOME",
                    href: "#home"
                },

                {
                    voice: "ABOUT",
                    href: "#about"
                },

                {
                    voice: "PROJECTS",
                    href: "#projects"
                },

                {
                    voice: "SERVICES",
                    href: "#services"
                },

                {
                    voice: "BLOG",
                    href: "#blog"
                },

                {
                    voice: "CONTACT",
                    href: "#contact"
                }
            ]
        }
    }
}
</script>


<!-- tempalte section -->
<template>
    <header data-aos="fade-down" data-aos-duration="1000"   id="home">
        <img src="../assets/images/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg" alt="consulting people" class="background-img">
        <nav class="mx-5 mb-5">
            <div class="logo" data-aos="fade-right" data-aos-easing="linear" data-aos-duration="2000" >
                <img src="../assets/images/logotype.png" alt="Phlox logo">
            </div>
            <ul>
                <li v-for="(item, index) in navigationLinks" :key="index">
                    <a class="text-white" :href="item.href">{{ item.voice }}</a>
                </li>
            </ul>
        </nav>
        <div class="jumbotron">
            <!-- jumbotron container -->
            <div class="jumbotron-container" data-aos="fade-up" data-aos-easing="linear" data-aos-duration="2000">
                <div class="titles-jumbotron">
                    <h3 class="pseudo">ALWATS THE BEST WAY YOU NEED IT</h3>
                    <h1>THE BEST<br>BUSINESS<br>CONSULTING</h1>
                </div>
                <div class="btn-jumbotron" data-aos="fade-right"  data-aos-duration="1500">
                    <a href="#"><button type="button" class="btn green-btn btn-lg rounded-0 py-3 px-5 me-4">READ MORE</button></a>
                    <a href="#"><i class="fa-solid fa-play rounded-circle p-4"></i></a>
                </div>
            </div>
            <!-- /jumbotron container -->
        </div>
    </header>
</template>
<!-- /tempalte section -->

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

// nav formatting section
nav{
    display: flex;
    justify-content: space-between;

    // list formatting section
    ul{
        display: flex;

        // list items
        li{
            padding: 1rem;
            color: $text;
            opacity: .5;
            border-top: 3px solid transparent;
            transition-duration: .5s;

            &:hover{
                opacity: 2;
                border-top: 3px solid white;
            }
        }
    }

    // logo formatting section
    .logo{
        padding: 1rem;

        // img formatting section
        img{
            width: 120px;
        }
    }

}

// header formatting section
header{
    
    // background image formatting section
    .background-img{
        position: absolute;
        width: 68%;
        height: 800px;
        max-height: 100%;
        object-fit: cover;
        top: 0px;
        right: 0px;
        z-index: -999;
    }
}

// jumbotron formatting section
.jumbotron{
    padding: 10rem 0;
    
    // h3, h1 tipography
    h3, h1{
        color: $text;
    }
    
    // jumbotron container formatting section
    .jumbotron-container{
        width: 80%;
        margin: 0 auto;

        // pseudo
        h3::before{
            content:"";
            display: inline-block;
            width: 33px;
            height: 3px;
            margin-right: 10px;
        }

        // h1 tipography
        h1{
            font-family: 'Bai Jamjuree', sans-serif;
            font-size: 4.5rem;
        }

        // h3 tipography
        h3{
            font-size: .8rem;
        }

        // paly botton formatting section
            i{
                border: 1px solid white;
                color: #39ffbf; 
            
        }
    }
}

</style>
<!-- /style section -->
