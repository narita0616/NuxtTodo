<template>
    <h1>{{ message }}</h1>
    <form>
        <input type="text" placeholder="メッセージ" v-model=message />
        <input type="submit" v-on:click.prevent="dispText" />
    </form>
</template>

<script setup lang="ts">
import { ref } from "vue";

const message = ref("");

const dispText  = () => {
    console.log(message.value);
}

</script>