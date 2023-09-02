<!-- script section -->
<script>

export default{
    name:"TheTestimonial",

    data(){
        return{
            testimonialList: [
                {
                    title: "Vera Duncan",
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel, numquam ipsam facere a eligendi dolorum necessitatibus aliquam autem quas expedita. Corrupti, nobis. Corrupti in amet blanditiis quibusdam vel id aliquid",
                    link: "oliver-ragfelt-488196-2.jpg",
                    mouse:false

                },
                
                {
                    title: "Francesco Cimino",
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel, numquam ipsam facere a eligendi dolorum necessitatibus aliquam autem quas expedita. Corrupti, nobis. Corrupti in amet blanditiis quibusdam vel id aliquid",
                    link: "oliver-ragfelt-488196-unsplash.jpg",
                    mouse:false
                },

                {
                    title: "Michael Black",
                    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel, numquam ipsam facere a eligendi dolorum necessitatibus aliquam autem quas expedita. Corrupti, nobis. Corrupti in amet blanditiis quibusdam vel id aliquid",
                    link: "12679.jpg",
                    mouse:false
                }
            ]
        }
    },

    methods:{

        changeMouse: function(item){
            console.log("ok");
            console.log(item.title);
            console.log(item.mouse);
            item.mouse = true;
            console.log(item.mouse);
        },

        deleteMouse: function(item){
            item.mouse = false;
        },

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
    <section>

        <!-- testimonial title block -->
        <div class="testimonial-title">
            <div class="container-subtitle d-flex justify-content-right align-items-center gap-2">
                <h2 class="text-align-right">TESTIMONIAL</h2>
                <div class="line-green"></div>
            </div>
            <h3>WHAT'S THE CUSTOMER SAY<br> ABOUT OUR WORK</h3>
        </div>
        <!-- /testimonial title block -->

        <!-- testimonial list block -->
        <div class="testimonial-list" data-aos="zoom-in-left" data-aos-duration="3000">
            <div class="testimonial" v-for="(item, index) in testimonialList" @mouseenter="changeMouse(item)" @mouseleave="deleteMouse(item)" :class="item.mouse ? `background-${index + 1}`: ''">
                <p>{{ item.description }}</p>
                <h4>{{ item.title }}</h4>
                <h5>Amazon inc.</h5>
            </div>
        </div>
        <!-- /testimonial list block -->

    </section>
    <!-- /section -->
</template>
<!-- /template section -->




<style lang ="scss" scoped>
    @use '../styles/partials/variables' as *;

    section{
        padding-top: 200px;

// testimonial title formatting section
.testimonial-title{
    margin-right: 50px;
    .container-subtitle{
        display: flex;
        justify-content: right;
    
        // h2 tipography
        h2{
            font-size: .8rem;
            text-align: right;
        }
    }

    // h3 tipography
    h3{
        text-align: right;
        font-size: 2rem;
        margin-top: 1.5rem;
    }

    // h2, h3 tipography
    h2, h3{
        color: $text;
    }

}

// testimonial list formatting section

.testimonial-list{
    background-color: white;
    display: flex;
    width: 98%;
    margin-left: auto;
    margin-top: 1.5rem;

    // testimonial
    .testimonial{
        width: 33%;
        height: 20%;
        padding: 3.5rem 3rem;
        transition-duration: 1s;
    }

    // p
    p{
        margin-bottom: 2rem;
        color: $paragraph;
    }

    // h4 tipography
    h4{
        margin-bottom: .5rem;
        color: #1f1e38;
    }

    // h5 tipography
    h5{
        color: #aaaaaa;
    }

}

// testimonial background formatting section
// background 1
.testimonial.background-1{
    background-image: url('../assets/images/oliver-ragfelt-488196-2.jpg');
    object-fit: cover;
    background-position: bottom;

    &:hover{
        background-position: center;
    }
}

// background 2
.testimonial.background-2{
    background-image: url('../assets/images/12679.jpg');
    object-fit: cover;
    background-position: bottom;

    &:hover{
        background-position: center;
    }
}

// background 3
.testimonial.background-3{
    background-image: url('../assets/images/oliver-ragfelt-488196-unsplash.jpg');
    object-fit: cover;
    background-position: bottom;
    
    &:hover{
        background-position: center;
    }
}
    
}
</style>
<!-- /style section -->