<script setup lant="ts">
const props = defineProps({
  name: {
    type: String,
  }
});
</script>

<template>
  <section class="section">
    <h2>{{ props.name }}さんのプロフィール</h2>
    <slot/>
  </section>
</template>

<style scoped>
.section {
 border: solid 2px red;
}
</style>
