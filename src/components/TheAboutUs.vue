<!-- script section -->
<script>

export default{
    // name
    name:"TheAboutUs",

    data(){
        return{

        }
    }
}
</script>
<!-- /script section -->


<!-- template section -->
<template>
    

    <!-- about us section -->
    <section class="about-us-section " id="about">

        <!-- img -->
        <div class="about-us">
            <img src="../assets/images/business-people-working-together-on-project-and-5FHSKBL.jpg" alt="people talking">
        </div>
        <!-- /img -->
    
        <!-- about us text -->
        <div class="about-us-text">

            <!-- container text -->
            <div class="container-text">
                <div class="container-subtitle d-flex align-items-center gap-2">
                    <div class="line-green"></div>
                    <h2>ABOUT US</h2>
                </div>
                <h3>WE MAKE YOUR STRATEGY WORK</h3>
                <p>When while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknow plants are noticed by when i hear the buzz of the title world among the stalks, and grow familiar indescribable forms of the insects, and flies, then i feel the presence of the Almighty.</p>
            </div>
            <!-- /container text -->

        </div>
        <!-- /about us text -->
            
    </section>
    <!-- /about us section -->
    
    <!-- help section -->
    <section class="help-section green-btn d-flex">

        <!-- help -->
        <div class="help">
            <div class="row row-cols-2 d-flex justify-content-center align-items-center">
                <div class="col-3"><h2>WE HELP TO DELIVER THE BUSINESS CASE</h2></div>
                <div class="col-4"><p>When while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknow.</p></div>
            </div>

        </div>
        <!-- /help -->

        <a href="#"><button type="button" class="btn red-btn btn-lg rounded-0 py-3 px-5 text-white">GET STARTED</button></a>
    </section>
    <!-- /help section -->

</template>
<!-- /template section -->




<style lang ="scss" scoped>
@use '../styles/partials/variables' as *;


.about-us-section{
    display: flex;

    
    .about-us{
        width: 60%;
        height: 530px;
        display: flex;
    
        
        img{
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    
    }

    .about-us-text{
        display: flex;
        flex-direction: column;
        justify-content: center;
        width: 40%;
        padding-left: 6rem;

        .container-text{
            width: 80%;
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
            line-height: 65px;
            font-weight: 700;
        }

        
        p{
            color: $paragraph;
        }
    }
    
}

.help-section{
    position: relative;
    .help{
        height: 300px;
        display: flex;
        align-items: center;
    }

    .row{
        margin-left: 0;
    }

    button{

        &:hover{
            background-color: #1f1e38;
        }
    }
        // anchor formatting section
        a{
            position: absolute;
            bottom: 0px;
            right: 0px;
            color: $text;
        }
        
        h2{
            font-family: 'Bai Jamjuree', sans-serif;
        }

        // h2, p tipography
        p{
                padding: 3rem 2rem;
                color: #1f1e38;
            }
            
        }
</style>
<!-- /style section -->