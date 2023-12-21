<template>
    <head>
        <Title>Post {{ id }}</Title>
    </head>
    <h2>Bienvenido al post no. {{ id }}</h2>
</template>
<script setup>
// get the id from the route
    const {id} = useRoute().params;
    definePageMeta({
        validate: async (route) => {
            const nuxtApp= useNuxtApp();
            // regular expression to validate if the id is a number
            return /^\d+$/.test(route.params.id);
        }
    })
</script>