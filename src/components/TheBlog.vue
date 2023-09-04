<!-- SCRIPT -->
<script>

export default{
    // NAME
    name:"TheBlog",

    data(){
        return{
            // ARRAY IMG CARDS
            blogListCards:[
                "startup-business-people-and-strategy-board-PAJ3P9K-1390x1042.jpg",
                "business-people-working-together-on-project-and-5FHSKBL-1390.jpg"
            ]
        }
    },
    
    methods:{

        // IMG PATH METHOD
        getImgsPath: function(url){
            return new URL(url, import.meta.url).href
        }
    }
}
</script>

<!-- TEMPLATE -->
<template>
    <section id="blog">

        <!-- BLOG -->
        <div class="blog">
            <div class="container-subtitle d-flex align-items-center gap-2">
                <div class="line-green"></div>
                <h2>BLOG</h2>
            </div>

            <!-- BLOG TITLE -->
            <div class="blog-title">
                <h3>THE RECENT NEWS YOU MUST READ IT</h3>
                <a href="#"><button type="button" class="btn green-btn btn-lg rounded-0 py-3 px-5 me-4">VIEW ALL</button></a>
            </div>
            

            <!-- BLOG CARDS -->
            <div class="blog-cards">
                <div class="row gx-0 row-cols-2">
                    <div class="col-12 d-flex justify-content-center gap-3">

                        <!-- CARDS V-FOR -->
                        <div class="card" v-for="(item, index) in blogListCards">
                            <img :src="getImgsPath(`../assets/images/${item}`)" alt="people">

                            <!-- CARD DESCRIPTION -->
                            <div class="description" data-aos="fade-up" data-aos-anchor-placement="top-bottom" data-aos-delay="1500" data-aos-duration="3000">
                                <h4>July 4, 2019 by Paul</h4>
                                <h2>Canadian Consulting Firm Acquired by UK Giant</h2>
                                <p>When while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a...</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div> 
        </div>
    </section>
</template>




<!-- STYLE -->
<style lang ="scss" scoped>
@use '../styles/partials/variables' as *;

// SECTION BLOG
section{

    // BLOG
    .blog{
        padding-top: 200px;
        padding-left: 50px;

        h2{
            font-size: 16px;
            font-weight: 400px;
            line-height: 25px;
            color: $text;
        }
        
        // BLOG TITLE
        .blog-title{
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: .5rem 0 3rem 0 ;

            h3{
                font-family: 'Bai Jamjuree', sans-serif;
                color: $text;
                font-size: 3rem;
            }

            button{

                &:hover{
                    color: white;
                    background-color: #f81d39;
                }
            }
        }

        // CARDS CONTAINER
        .blog-cards{
            display: flex;
            justify-content: center;
            
            // CARDS
            .card{
                width: 45%;
                position: relative;

                img{
                    max-width: 100%;
                }
            }
            
            // DESCRIPTION CARDS
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

                h4{
                    color: #f81d39;
                }

                h2{
                    font-family: 'Bai Jamjuree', sans-serif;
                    color: #1f1e38;;
                }

                p{
                    color: grey;
                }
            }
        }
    }
}
</style>
