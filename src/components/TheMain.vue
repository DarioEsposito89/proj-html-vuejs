<!-- script section -->
<script>

// import vue components codes
import TheConsultants from './TheConsultants.vue'
import TheAboutUs from './TheAboutUs.vue';

export default{
    // name
    name: "TheMain",

    components:{
        TheConsultants,
        TheAboutUs,
        
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
    </main>
    <!-- /main section -->

</template>
<!-- /template section -->



<!-- style section -->
<style lang="scss" scoped>
</style>
<!-- /style section -->