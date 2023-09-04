<!-- SCRIPT -->
<script>

export default {
    // NAME
    name: "TheFooter",

    data() {
        return {
            // ARRAY LINKS
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

            // ARRAY ICONS SOCIAL
            socialIcons: [
                "fa-brands fa-instagram",
                "fa-brands fa-linkedin",
                "fa-brands fa-facebook",
                "fa-brands fa-twitter"
            ],
        }
    },
}
</script>

<!-- TEMPLATE -->
<template>
    <section>
        <!-- FOOTER TOP -->
        <div class="container footer-top">
            <div class="row row-cols-3 gx-0 d-flex justifi-content-between align-items-center">

                <!-- LOGO -->
                <div class="col-3 footer-logo d-flex justify-content-start">
                    <a href="" id="home">
                        <img src="../assets/images/logotype-2-139x23.png" alt="Phlox footer logo image">
                    </a>
                </div>
                
                <!-- LINKS -->
                <ul class="col-6 links d-flex justify-content-center align-items-center gap-4">
                    <!-- V-FOR PRINT LINKS -->
                    <li v-for="(item, index) in footerLinks" class="links-voices">
                        <a :href="item.href">{{ item.voice }}</a>
                    </li>
                </ul>

                <!-- SOCIAL -->
                <ul class="col-3 social d-flex justify-content-end align-items-center gap-4">
                    <!-- V-FOR PRINT INCONS SOCIAL -->
                    <li v-for="(item, index) in socialIcons">
                        <a href="#"><i :class="item"></i></a>
                    </li>
                </ul>
            </div>
        </div>
    </section>

    <!-- FOOTER BOTTOM -->
    <section>
        <div class="container footer-bottom">

            <!-- LINE DIVISOR -->
            <hr>

            <div class="row row-cols-2 gx-0 d-flex justify-content-between ">

                <!-- POLICY PRIVACY -->
                <div class="col-5 terms">
                    <p>Terms of use</p>
                    <p>Privacy Environment Policy</p>
                </div>

                <!-- COPYRIGHT -->
                <div class="col-5 copyright d-flex justify-content-end align-items-center">
                    <p>Copyright @ 2020 Phlox Consulting. All Rights Reserved.</p>
                </div>
            </div>
        </div>
    </section>
</template>


<!-- STYLE -->
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
</style>
