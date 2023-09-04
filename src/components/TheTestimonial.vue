<!-- SCRIPT -->
<script>

export default{
    // NAME
    name:"TheTestimonial",

    data(){
        return{
            // ARRAY OVERLAY ELEMENTS
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
            item.mouse = true;
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



<!-- TEMPLATE -->
<template>
    <section>
        <!-- TITLES -->
        <div class="testimonial-title">
            <div class="container-subtitle d-flex justify-content-right align-items-center gap-2">
                <h2 class="text-align-right">TESTIMONIAL</h2>
                <div class="line-green"></div>
            </div>
            <h3>WHAT'S THE CUSTOMER SAY<br> ABOUT OUR WORK</h3>
        </div>

        <!-- TESTIMONIAL -->
        <div class="testimonial-list">
            <div class="testimonial" v-for="(item, index) in testimonialList" @mouseenter="changeMouse(item)" @mouseleave="deleteMouse(item)" :class="item.mouse ? `background-${index + 1}`: ''">
                <p>{{ item.description }}</p>
                <h4>{{ item.title }}</h4>
                <h5>Amazon inc.</h5>
            </div>
        </div>
    </section>
</template>

<!-- STYLE -->
<style lang ="scss" scoped>
    @use '../styles/partials/variables' as *;

    section{
        padding-top: 200px;

// TITLES
.testimonial-title{
    margin-right: 50px;
    .container-subtitle{
        display: flex;
        justify-content: right;
    
        h2{
            font-size: 16px;
            font-weight: 400px;
            line-height: 25px;
            text-align: right;
        }
    }

    h3{
        font-family: 'Bai Jamjuree', sans-serif;
        text-align: right;
        font-size: 3rem;
        margin-top: 1.5rem;
    }

    h2, h3{
        color: $text;
    }

}

// TESTIMONIAL
.testimonial-list{
    background-color: white;
    display: flex;
    width: 98%;
    margin-left: auto;
    margin-top: 1.5rem;

    .testimonial{
        width: 33%;
        height: 20%;
        padding: 3.5rem 3rem;
        transition-duration: 1s;
    }

    p{
        margin-bottom: 2rem;
        color: $paragraph;
    }

    h4{
        font-family: 'Bai Jamjuree', sans-serif;
        margin-bottom: .5rem;
        color: #1f1e38;
    }

    h5{
        color: #aaaaaa;
    }

}

// TESTIMONIAL BACKGROUND

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
