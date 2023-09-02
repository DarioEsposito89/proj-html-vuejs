<!-- script section -->
<script>

// import vue components codes
import TheConsultants from './TheConsultants.vue';
import TheAboutUs from './TheAboutUs.vue';
import TheProject from './TheProject.vue';
import TheTestimonial from './TheTestimonial.vue';
import TheBlog from './TheBlog.vue';
import TheTalkAboutWork from './TheTalkAboutWork.vue';


export default{
    // name
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
<!-- /script section -->



<!-- tempalte section -->
<template>
    
    <!-- main -->
    <main>
        <TheConsultants></TheConsultants>
        <TheAboutUs></TheAboutUs>
        <TheProject></TheProject>
        <TheTestimonial></TheTestimonial>
        <TheBlog></TheBlog>
        <TheTalkAboutWork></TheTalkAboutWork>

        
    </main>
    <!-- /main section -->

</template>
<!-- /template section -->



<!-- style section -->
<style lang="scss" scoped>
</style>
<!-- /style section -->