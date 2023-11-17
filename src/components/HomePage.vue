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
    const index = Math.floor(Math.random() * secretMessages.length);
    secretMessage.value = secretMessages[index]
    window.setTimeout(() => { secretMessage.value = ''  }, 1000)
}

const secretMessages = [
    'I love you',
    "It's okay, fish",
    'You are always loved',
    "Things are never as bad as they seem",
    "You've got this!",
    'I believe in you',
    'I hope your UTI feels better soon',
    "You're being very brave",
    "It's lonely here without you",
    "Team Rob & Emma",
    "Shhhlluuuuuuurrrrrrp"
]

</script>

<style scoped>
.space {
    padding: 10px;
}

.button {
    color: teal;
}
</style>