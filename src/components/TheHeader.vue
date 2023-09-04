<script>
import { store } from '/store.js'

export default {
    // NAME
    name: "TheHeader",
    components: {
        store,
    },
    data() {
        return {
            // ARRAY LINKS
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
    },
    methods: {
        // FUNCTION TO RETURN TO THE HEADER
        scrollTop() {
            window.scrollTo(0, 0);
        },
    }
}
</script>


<!-- TEMPLATE -->
<template>
    <!-- HEADER -->
    <header id="home">

        <!-- IMG HEADER -->
        <img src="../assets/images/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg" alt="consulting people" class="background-img">

        <!-- NAVBAR -->
        <nav class="mx-5 mb-5">
            <!-- LOGO -->
            <div class="logo">
                <img src="../assets/images/logotype.png" alt="Phlox logo">
            </div>
            <!-- LIST LINKS -->
            <ul>
                <!-- V-FOR PRINT LINKS -->
                <li v-for="(item, index) in navigationLinks" :key="index">
                    <a class="text-white" :href="item.href">{{ item.voice }}</a>
                </li>
            </ul>
        </nav>

        <!-- JUMBOTRON -->
        <div class="jumbotron ms-5">
            <div class="jumbotron-container">

                <!-- TITLES -->
                <div class="titles-jumbotron">
                    <div class="container-subtitle d-flex align-items-center gap-2">
                        <div class="line-green"></div>
                        <h3>ALWATS THE BEST WAY YOU NEED IT</h3>
                    </div>
                    <h1>THE BEST<br>BUSINESS<br>CONSULTING</h1>
                </div>
                
                <!-- BUTTONS -->
                <div class="btn-jumbotron">
                    <a href="#"><button type="button" class="btn green-btn btn-lg rounded-0 py-3 px-5 me-4">READ MORE</button></a>
                    <a href="#"><i class="fa-solid fa-play rounded-circle p-4"></i></a>
                </div>
            </div>
        </div>
    </header>

    <!-- ICON FIXED -->
    <section>
        <div class="icon-fixed d-flex justify-content-end gap-5 p-5 fixed-bottom fixed-right">
            <!-- ARROW SCROLL TOP -->
            <i class="fa-solid fa-arrow-up icon-arrow" @click="scrollTop"></i>

            <!-- CHAT -->
            <i class="fa-regular fa-comment icon-comment"></i>
        </div>
    </section>

    <!-- LATERAL BUTTONS FIXED -->
    <div class="sticky-button">
        <div class="button-fixed">
            <a href="#">
                <img src="https://demo.phlox.pro/consulting-2/wp-content/plugins/demo-tools/public/assets/img/Group-3.svg">
                <span>Browse Demos</span>
            </a>
        </div>
        <div class="button-fixed">
            <a href="#">
                <img src="https://demo.phlox.pro/consulting-2/wp-content/plugins/demo-tools/public/assets/img/buy.svg">
                <span>Buy Now!</span>
            </a>
        </div>
        <div class="button-fixed">
            <a href="#">
                <img src="https://demo.phlox.pro/consulting-2/wp-content/plugins/demo-tools/public/assets/img/export.svg">
                <span>Export Section</span>
            </a>
        </div>
    </div>
</template>

<!-- STYLE -->
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

// NAVBAR
nav{
    display: flex;
    justify-content: space-between;

    // LIST LINKS
    ul{
        display: flex;

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

    // LOGO
    .logo{
        padding: 1rem;

        img{
            width: 120px;
        }
    }

}

// HEADER
header{
    
    .background-img{
        position: absolute;
        width: 72%;
        height: 846px;
        min-height: 100%;
        object-fit: cover;
        top: 0px;
        right: 0px;
        z-index: -999;
    }
}

// JUMBOTRON
.jumbotron{
    padding: 10rem 0;
    
    h3, h1{
        color: $text;
    }
    
    .jumbotron-container{
        width: 80%;
        padding-left: 1rem;

        
        h1{
            font-family: 'Bai Jamjuree', sans-serif;
            font-size: 106px;
            font-weight: 700px;
            line-height: 93px;
        }

        
        h3{
            font-size: 16px;
            font-weight: 400px;
            line-height: 19px;
            letter-spacing: 2.8px;
        }

        // BUTTONS HEADER
        button{
            &:hover{
                color: $text;
                background-color: $icon-consultants-color;
            }
        }

            i{
                border: 1px solid white;
                color: #39ffbf; 
            
        }
    }
}

// ICONS FIXED
.icon-fixed{
    
    .fa-arrow-up{
            background-color: white;
            border: 1px solid black;
            border-radius: 50%;
            width: 30px;
            height: 30px;
            line-height: 30px;
            text-align: center;
            margin-left: 10px;
            

            &:hover{
                background-color: rgb(85, 85, 85);
                color: white;
            }
        }   
        
        

    // CHAT
    .fa-comment{
            background-color: #527ceb;
            color: white;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            line-height: 50px;
            text-align: center;
            margin-left: 10px;
        }    
}

// LATERAL BUTTONS FIXED
.aux-preview-button {
    transition-delay: 50ms;
}
.sticky-button{
    position: fixed;
    right: 0;
    top: 50%;
    z-index: 9999;
    transform: translate(20px,-50%);

        .button-fixed{
            border-radius: 8px 0 0 8px;
            opacity: 1;
            margin-bottom: 6px;
            height: 40px;
            width: 152px;
            line-height: 40px;
            text-transform: capitalize;
            font-size: 13px;
            font-family: 'Raleway',sans-serif;
            overflow: hidden;
            min-width: 145px;

            a{
                width: 100%;
                position: relative;
                font-size: 12px;
                color: white;
                padding-left: 20px;
                display: flex;
                align-items: center;
                gap: .5rem;
                background-color: rgba(67, 67, 67, 0.551);
                
            }

            a:hover{
                background-color: blue;
            }

            a:before{
                position: absolute;
                content: '';
                display: inline-block;
                top: -180px;
                left: 0;
                width: 30px;
                height: 100%;
                background-color: #fff;
                animation: shiny-btn1 3s ease-in-out infinite;
            }
            @-webkit-keyframes shiny-btn1 {
                0% { -webkit-transform: scale(0) rotate(45deg); opacity: 0; }
                80% { -webkit-transform: scale(0) rotate(45deg); opacity: 0.5; }
                81% { -webkit-transform: scale(4) rotate(45deg); opacity: 1; }
                100% { -webkit-transform: scale(50) rotate(45deg); opacity: 0; }
            }
        }
    }
</style>

