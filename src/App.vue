<script>
import Calculator from "./components/Calculator.vue";

export default {
   components: {
      Calculator,
   },
};
</script>

<template>
   <div class="main"><Calculator /></div>
</template>

<style scoped>
.main {
   width: 100vw;
   height: 100vh;
}
</style>
