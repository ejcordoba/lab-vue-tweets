<template>
  <span className="user">
    <span className="name">{{ name }}</span>
    <span className="handle">@{{ handle }}</span>
  </span>
</template>

<script setup>
const props = defineProps(["name", "handle"]);
</script>

<style lang="scss" scoped></style>
