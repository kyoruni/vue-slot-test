<script setup lant="ts">
const props = defineProps({
  name: {
    type: String,
  }
});

const familyInfo = {
  num: 4,
  memo: "両親と妹との四人暮らし",
};
const families = ["母：恵美子", "父：宗介", "妹：美香"];
</script>

<template>
  <section class="section">
    <h2>{{ props.name }}さんのプロフィール</h2>
    <!-- default slot -->
    <slot>
      <p>まだプロフィールが記入されていません。</p>
    </slot>
    <!-- detail slot -->
    <slot name="detail">
      <p>まだ詳細情報が記入されていません。</p>
    </slot>
    <!-- スコープ付きslot（子から親にデータを渡す） -->
    <slot name="scope" :familyInfo="familyInfo">
      <h4>家族構成</h4>
      <ul>
        <li>num：{{ familyInfo.num }}</li>
        <li>memo：{{ familyInfo.memo}}</li>
      </ul>
    </slot>
  </section>
</template>

<style scoped>
.section {
  background: #f2f2f2;
  border-radius: 5px;
  padding: 10px;
  margin: 10px;
}
</style>
