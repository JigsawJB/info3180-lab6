<script>

import NewList from '@/components/NewsList.vue'

export default {
    data() {
        return {
            message: "Hello Sir! Welcome to my VueJS. You can call me Jigsaw."
        };
    },
    components: { NewList }
}
</script>

<template>
    <div class="container">
      <div class="text-center">
        <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />
        <h1>{{ message }}</h1>
        <NewList />
      </div>
    </div>
</template>

<style>
/* Add any component specific styles here */
</style>