<template>
    <div class="background">
        <p class="space">Hi, Emma!</p>
        <v-chip class="space button" @click="onClick">Click me</v-chip>
        <p class="space">{{secretMessage}}</p>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const secretMessage = ref('')

function onClick(){
    secretMessage.value = 'I love you!'
    window.setTimeout(() => { secretMessage.value = ''  }, 1000)
}

</script>

<style scoped>
.space {
    padding: 10px;
}

.button {
    color: teal;
}
</style>