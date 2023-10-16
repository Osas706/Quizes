<script setup>
 import{defineProps} from "vue";
 import{RouterLink} from "vue-router"

 const {numberOfCorrectAnswers, quizQuestionLength} = defineProps(["quizQuestionLength", "numberOfCorrectAnswers"]) 
</script>

<template>
    <div class="results">
        <p>Your Results</p>
        <h1>
            {{ numberOfCorrectAnswers}}/{{ quizQuestionLength }}
        </h1>

        
        <router-link class="home" to="/">Home</router-link>      
    </div>
</template>

<style scoped>
.results{
    text-align: center;
    padding: 100px 0;
}

p{
    font-size: 25px;
}

h1{
    font-size: 80px;
}

.home {
    text-decoration: none;
    color: black;
    font-size: 20px;
    background-color: bisque;
    padding: 10px 20px;
    border-radius: 10px;  
}
</style>