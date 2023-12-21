<template>
  <div>
    <h1>ops! Error</h1>
    <h3>{{ error.statusCode }} - {{ error.statusMessage }}</h3>
    <button @click="handleError">Clean error</button>
  </div>
</template>

<script setup>
// get information from the router
const route = useRouter();
const path  = route.path == error.url ? "/" : route.path;
// create object error
const { error } = defineProps({
  error: Object,
});
console.log(error);
// handle error, return to home
const handleError = () => {
    console.log("handleError");
  clearError({
    redirect: "/",
  });
};

</script>

<style scoped>
div {
  margin: 0 auto;
  width: 50%;
  text-align: center;
}
</style>
