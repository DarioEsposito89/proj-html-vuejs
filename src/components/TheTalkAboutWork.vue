<!-- SCRIPT -->
<script>

export default{
    // NAME
    name: "TheTalkAboutWork",

    data(){
        return{

        }
    }
}
</script>

<!-- TEMPLATE -->
<template>
    <section>
        <h2>LET'S TALK ABOUT WORK</h2>
        <p>A Wonderful serenity has taken possession Far far away, behind the world mountains.</p>
        <a href="#"><button type="button" class="btn btn-lg rounded-0 py-3 px-5">GET STARTED</button></a>
    </section>
</template>




<!-- STYLE -->
<style lang ="scss" scoped>
@use '../styles/partials/variables' as *;


section{
    padding: 7rem 0;
    margin-top: 250px;
    background-image: url('../assets/images/business-people-working-together-on-project-and-B3MZ4TX.jpg');
    background-size: cover;
    display: flex;
    flex-direction: column;
    align-items: center;
    color: $text;

    h2{
        font-family: 'Bai Jamjuree', sans-serif;
        font-size: 3rem;
    }

    p{
        color: $paragraph;
        padding-top: 1rem;
    }

    button{
        color: white;
        background-color: #1f1e38;
    

        &:hover{
            color: #1f1e38;
            background-color: #39ffbf;
        }
    }

}
</style>
