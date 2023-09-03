
<script>

export default {
    // naame
    name: "TheFooter",

    data() {
        return {
            // array
            footerLinks: [
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
            ],

            // array
            socialIcons: [
                "fa-brands fa-instagram",
                "fa-brands fa-linkedin",
                "fa-brands fa-facebook",
                "fa-brands fa-twitter"
            ],
        }
    },
    methods: {
        scrollTop() {
            window.scrollTo(0, 0);
        },
    }
}
</script>


<template>
    <section>

    <!-- footer top  -->
        <div class="container footer-top">
            <div class="row row-cols-3 gx-0 d-flex justifi-content-between align-items-center">
                <!-- logo -->
            <div class="col-3 footer-logo d-flex justify-content-start">
                <a href="" id="home">
                    <img src="../assets/images/logotype-2-139x23.png" alt="Phlox footer logo image">
                </a>
            </div>
            <!-- /logo -->

            <!-- links -->
            <ul class="col-6 links d-flex justify-content-center align-items-center gap-4">
                <li v-for="(item, index) in footerLinks" class="links-voices">
                    <a :href="item.href">{{ item.voice }}</a>
                </li>
            </ul>
            <!-- /links -->

            <!-- social -->
            <ul class="col-3 social d-flex justify-content-end align-items-center gap-4">
                <li v-for="(item, index) in socialIcons">
                    <a href="#"><i :class="item"></i></a>
                </li>
            </ul>
            <!-- /social -->
            </div>
        </div>
        <!-- /footer top -->

    </section>

    <section>

        <div class="container footer-bottom">
            <hr>
            <div class="row row-cols-2 gx-0 d-flex justify-content-between ">
                <div class="col-5 terms">
                    <p>Terms of use</p>
                    <p>Privacy Environment Policy</p>
                </div>

                <div class="col-5 copyright d-flex justify-content-end align-items-center">
                    <p>Copyright @ 2020 Phlox Consulting. All Rights Reserved.</p>
                </div>
                <i class="fa-solid fa-arrow-up icon-arrow" @click="scrollTop"></i>
                <i class="fa-regular fa-comment icon-comment" @click="showChat"></i>
                
            </div>
            
            

        </div>

    </section>

</template>







<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

// FOOTER TOP
.container{
    padding-top: 50px;
    padding-bottom: 25px;

    .links{
        align-items: center;
    }

    ul{
        margin-bottom: 0;
    }

    .links{
        a{
            color: $paragraph;

            &:hover{
                color: $icon-consultants-color;
            }
        }
    }

    .social{
        a{
            color: $text;

            &:hover{
                color: $icon-consultants-color;
            }
        }
    }
    
}

// FOOTER BOTTOM
hr{
    color: $paragraph;
    margin-bottom: 50px;
}
.row{
    position: relative;
}
.terms{
    color: $paragraph;
}

.copyright{
    color: $paragraph;
}

p{
    margin-bottom: 0;
}


    // arrow up formatting section
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

    // message formatting gsection
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
    

</style>
