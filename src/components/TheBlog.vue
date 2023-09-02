<!-- script section -->
<script>

export default{
    name:"TheBlog",

    data(){
        return{
            // array
            blogListCards:[
                "startup-business-people-and-strategy-board-PAJ3P9K-1390x1042.jpg",
                "business-people-working-together-on-project-and-5FHSKBL-1390.jpg"
            ]
        }
    },
    // methods
    methods:{

        // images path method
        getImgsPath: function(url){
            return new URL(url, import.meta.url).href
        }
    }
}
</script>
<!-- /script section -->



<!-- template section -->
<template>
    <!-- section -->
    <section id="blog">

        <!-- blog -->
        <div class="blog">
            <div class="container-subtitle d-flex align-items-center gap-2">
                <div class="line-green"></div>
                <h2>BLOG</h2>
            </div>

            <!-- blog title -->
            <div class="blog-title">
                <h3>THE RECENT NEWS YOU MUST READ IT</h3>
                <a href="#"><button type="button" class="btn green-btn btn-lg rounded-0 py-3 px-5 me-4">VIEW ALL</button></a>
            </div>
            <!-- /blog title -->

            <!-- blog cards -->
            <div class="blog-cards">
                <div class="row row-cols-2">
                    <div class="col-12 d-flex justify-content-center gap-3">
                        <!-- general card -->
                        <div class="card" v-for="(item, index) in blogListCards">
                        <img :src="getImgsPath(`../assets/images/${item}`)" alt="people">
                        <!-- general card description -->
                        <div class="description" data-aos="fade-up" data-aos-anchor-placement="top-bottom" data-aos-delay="1500" data-aos-duration="3000">
                            <h4>July 4, 2019 by Paul</h4>
                            <h2>Canadian Consulting Firm Acquired by UK Giant</h2>
                            <p>When while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a...</p>
                        </div>
                        <!-- /general card description -->
                        </div>
                <!-- /general card -->
                    </div>
                    

                </div>

                
            </div> 
            <!-- /blog cards -->

        </div>
        <!-- /blog -->

    </section>
    <!-- /section -->
</template>
<!-- /template section -->



<!-- style section -->
<style lang ="scss" scoped>
@use '../styles/partials/variables' as *;

// section formatting
section{

    // blog formatting section
    .blog{
        padding-top: 200px;
        padding-left: 50px;

        // h2 tipography
        h2{
            font-size: .8rem;
        }
        
        // h2 tipography
        h2{
            color: $text;
        }

        // blog title formatting section
        .blog-title{
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: .5rem 0 3rem 0 ;

            // h3 tipography
            h3{
                color: $text;
                font-size: 2rem;
            }
        }

        // blog cards formatting section
        .blog-cards{
            display: flex;
            justify-content: center;
            
            // general card formatting section
            .card{
                width: 45%;
                position: relative;

                // image formatting section
                img{
                    max-width: 100%;
                }
            }
            
            // description formatting section
            .description{
                width: 80%;
                background-color: rgba(255, 255, 255);
                position: absolute;
                bottom: -100px;
                right: 0px;
                padding: 2rem 3rem;

                    &:hover{
                        background-color: #39ffbf;
                    }

                // h4 tipography
                h4{
                    color: #f81d39;
                }

                // h2 tipography
                h2{
                    color: #1f1e38;;
                }

                // p
                p{
                    color: grey;
                }
            }
        }
    }
}

</style>
<!-- /style section -->