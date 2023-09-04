<!-- SCRIPT -->
<script>

// IMPORT VUE COMPONENTS
import TheConsultants from './TheConsultants.vue';
import TheAboutUs from './TheAboutUs.vue';
import TheProject from './TheProject.vue';
import TheTestimonial from './TheTestimonial.vue';
import TheBlog from './TheBlog.vue';
import TheTalkAboutWork from './TheTalkAboutWork.vue';


export default{
    // NAME
    name: "TheMain",

    components:{
        TheConsultants,
        TheAboutUs,
        TheProject,
        TheTestimonial,
        TheBlog,
        TheTalkAboutWork,
        
        
    }
}
</script>

<!-- TEMPLATE -->
<template>
    
    <main>
        <TheConsultants></TheConsultants>
        <TheAboutUs></TheAboutUs>
        <TheProject></TheProject>
        <TheTestimonial></TheTestimonial>
        <TheBlog></TheBlog>
        <TheTalkAboutWork></TheTalkAboutWork>
    </main>

</template>

<!-- STYLE -->
<style lang="scss" scoped>

</style>
