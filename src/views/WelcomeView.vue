<script setup lang="ts">

import { ref } from 'vue';

const greeting = "Welcome to this site";
let message = ref('This site contains information about available jobs.');

const showButton = ref(true);

const changeMessage = () => {
  message.value = 'This site also contains skills you need for IT jobs.';
  showButton.value = false;
}



</script>
 
<template>
    <div class="welcome">
        <h2>{{ greeting }}</h2>
        <p>{{ message }}</p>
        <div class="button-container" >
            <button class="border-gradient border-gradient-green" v-if="showButton" @click="changeMessage">more info</button>
            
        </div>
    </div>
</template>

<style scoped>
    h2 {
        color: rgb(255, 200, 0);
        margin-bottom: 2rem;
    }
 
    p {
        color: #aaa;
        font-style: italic;
        margin-bottom: 2rem;
    }

    button {
      background: none;
      text-decoration: inherit;
      font-family: system-ui;
      font-size: 1rem;
      padding: 1rem 2rem;
      color: white;
      text-transform: uppercase;
    }
    .button-container {
        width: 100%;
        padding: 1rem;
    }
    .border-gradient {
      border: 10px solid;
      border-image-slice: 1;
      border-width: 5px;
    }
    .border-gradient-purple {
      border-image-source: linear-gradient(to left, #743ad5, #d53a9d);
    }
    .border-gradient-green {
      border-image-source: linear-gradient(to left, #00C853, #B2FF59);
    }
</style>