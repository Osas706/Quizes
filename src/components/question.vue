<script setup>
  import {defineProps, defineEmits} from "vue";

  const emit = defineEmits(["selectOption"]);

  const emitSelectedOption = (isCorrect) => {
    emit("selectOption", isCorrect)
  };
   
  const { question} = defineProps(['question'])
</script>

<template> 
    <div class="question-container">
        <h1 class="question">
            {{question.text}}
        </h1>
    </div>

    <div class="options-container">
        <div v-for="option in question.options" :key="option.id"      
         @click="emitSelectedOption(option.isCorrect)" class="options" >
            <p class="option-label">{{option.label}}</p>
            <div class="option-value">
                <p>{{option.text}}</p>
            </div>
        </div>
    </div>
</template> 

<style scoped>
.question-container{
    margin-top: 20px;  
}

.question{
    font-size: 40px;
    margin-bottom: 20px;
}

/**************************************** */
.options{
    display: flex;
    margin-bottom: 20px;
    cursor: pointer;
    gap: 10px;
}

.option-label{
background-color: bisque;
width: 50px;
height: 50px;
font-size: 30px;
display: flex;
align-items: center;
justify-content: center;
color: black;
}

.option-value{
    background-color: rgb(244, 239, 239);
    width: 100%;
    font-size: 20px;
    padding: 0 20px;
    display: flex;
    align-items: center;
    color: black;
}
</style>