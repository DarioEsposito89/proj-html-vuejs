
<script>

export default{
    // naame
    name: "TheFooter",

    data(){
        return{
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
            ]
        }
    }
}
</script>


<template>
    <section>

    <!-- footer top  -->
    <div class="footer-top">
        <div class="row row-cols-3 gx-0 d-flex justifi-content-between align-items-center">
            <!-- logo -->
        <div class="col-3 footer-logo">
            <a href="" id="home">
                <img src="../assets/images/logotype-2-139x23.png" alt="Phlox footer logo image">
            </a>
        </div>
        <!-- /logo -->

        <!-- links -->
        <ul class="col-6 links d-flex justify-content-center gap-4">
            <li v-for="(item, index) in footerLinks" class="links-voices">
                <a :href="item.href">{{ item.voice }}</a>
            </li>
        </ul>
        <!-- /links -->

        <!-- social -->
        <ul class="col-3 social d-flex justify-content-center gap-4">
            <li v-for="(item, index) in socialIcons">
                <a href="#"><i :class="item"></i></a>
            </li>
        </ul>
        <!-- /social -->
        </div>
    </div>
    <!-- /footer top -->

    </section>
    <!-- /section -->
</template>
<!-- /template section -->






<style lang="scss" scoped>

.row{
    
}

</style>
