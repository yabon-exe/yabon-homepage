<script setup>
  const buildTime = "202303132030";
  defineExpose({
    buildTime
  });
</script>

<template>
  <p class="ver">ver: {{ buildTime }}</p>
</template>

<style lang="scss">
.ver {
  position: fixed;
  top: 0px;
  left: 5px;
  z-index: 5;
}
</style>