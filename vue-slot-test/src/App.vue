<script setup lang="ts">
import Section from '@/components/Section.vue';
</script>

<template>
  <div id="app">
    <Section name="田中太郎">
      <!-- default slot -->
      <template #default>
        <ul>
          <li>性別：男</li>
          <li>年齢：28</li>
          <li>出身：神奈川県横浜市</li>
      </ul>
      </template>
      <!-- detail slot -->
      <template #detail>
        <ul>
          <li>実家は秋田県らしい</li>
          <li>趣味はバイク</li>
        </ul>
      </template>
    </Section>
    <Section name="山田花子"/>
  </div>
</template>
