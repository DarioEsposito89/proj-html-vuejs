<!-- script section -->
<script>

// import vue components codes
import TheConsultants from './TheConsultants.vue';
import TheAboutUs from './TheAboutUs.vue';
import TheProject from './TheProject.vue';
import TheTestimonial from './TheTestimonial.vue';


export default{
    // name
    name: "TheMain",

    components:{
        TheConsultants,
        TheAboutUs,
        TheProject,
        TheTestimonial,
        
        
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
        <TheTestimonail></TheTestimonail>
        
    </main>
    <!-- /main section -->

</template>
<!-- /template section -->



<!-- style section -->
<style lang="scss" scoped>
</style>
<!-- /style section -->