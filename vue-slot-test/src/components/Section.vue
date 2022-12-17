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
    <slot>
      <p>まだプロフィールが記入されていません。</p>
    </slot>
  </section>
</template>

<style scoped>
.section {
 border: solid 2px red;
}
</style>
