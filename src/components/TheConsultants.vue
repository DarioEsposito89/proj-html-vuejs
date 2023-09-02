<!-- script section -->
<script>

// import vue components codes
import { store } from '/store';
export default{
    // name
    name: "TheConsultats",

    components:{
        store,
    },
    data() {
        return {
            consultansLinks: [

                {
                    title: "STATISTICAL CONSULTING",
                    subtitle: "When while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a",
                    icon: "fa-solid fa-chart-line"
                },

                {
                    title: "DIGITAL CONSULTING",
                    subtitle: "When while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a",
                    icon: "fa-solid fa-bullhorn"
                },

                {
                    title: "BANKING CONSULTING",
                    subtitle: "When while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a",
                    icon: "fa-solid fa-wallet"
                },

                {
                    title: "ENTERPRICE CONSULTING",
                    subtitle: "When while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a",
                    icon: "fa-solid fa-bullseye"
                }

            ]
        }
    }
}
</script>
<!-- /script section -->



<!-- tempalte section -->
<template>
    <section class="bg-white ms-5">
        <div class="container-consultants">
            <div class="container-title d-flex align-items-center gap-4 mb-2">
                <h2 class="pseudo">OUR CONSULTANTS CAN HELP YOU</h2>
                <div class="line-divider"></div>
            </div>
            
            <div class="container">
                <div class="row row-cols-2 ">
                    <div class="col-5 d-flex gap-5 py-5" v-for="(item, index) in consultansLinks" :key="index">
                        <div class="icon me-2 mt-3">
                            <a class="rounded-circle p-3" href="#"><i :class="item.icon"></i></a>
                        </div>
                        <div class="description ms-2">
                            <h3 class="mb-3">{{ item.title }}</h3>
                            <p>{{ item.subtitle }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

</template>
<!-- /template section -->



<!-- style section -->
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.line-divider{
    height: 3px;
    width: 798px;
    background-color: #39ffbf;
}
.container-consultants{
    padding-left: 100px;
    padding-top: 100px;
    padding-bottom: 150px;
}

h2{
    font-family: 'Bai Jamjuree', sans-serif;
}

a{
    color: white;
    background-color: $icon-consultants-color;
    font-size: 1.5rem;
}

h3{
    font-family: 'Bai Jamjuree', sans-serif;
}

p{
    font-size: 16px;
    font-weight: 400px;
    line-height: 25px;
}

</style>
<!-- /style section -->