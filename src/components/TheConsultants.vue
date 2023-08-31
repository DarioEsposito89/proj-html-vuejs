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
                    subtitle: "When while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknow plants are noticed by when i hear the buzz of the title.",
                    icon: "fa-solid fa-chart-line"
                },

                {
                    title: "DIGITAL CONSULTING",
                    subtitle: "When while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknow plants are noticed by when i hear the buzz of the title.",
                    icon: "fa-solid fa-bullhorn"
                },

                {
                    title: "BANKING CONSULTING",
                    subtitle: "When while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknow plants are noticed by when i hear the buzz of the title.",
                    icon: "fa-solid fa-wallet"
                },

                {
                    title: "ENTERPRICE CONSULTING",
                    subtitle: "When while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknow plants are noticed by when i hear the buzz of the title.",
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
    <section class="bg-white">
        <h2 class="pseudo mb-5">OUR CONSULTANTS CAN HELP YOU</h2>
        <div class="container">
            <div class="row row-cols-2">
                <div class="col d-flex gap-3" v-for="(item, index) in consultansLinks" :key="index">
                    <div class="icon">
                        <a href="#"><i :class="item.icon"></i></a>
                    </div>
                    <div class="description">
                        <h3>{{ item.title }}</h3>
                        <p>{{ item.subtitle }}</p>
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
.i {
    font-size: 3rem;
    color: white;
    background-color: $icon-consultants-color;
    border-radius: 0;
}

</style>
<!-- /style section -->