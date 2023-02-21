<script setup lang="ts">
  defineProps<{
    title: string,
    content: Object
  }>()
</script>

<template>
  <section class="box">
   <h2 class="headingL box__title">{{ title }}</h2>
   {{ content }}
  </section>
</template>

<style lang="scss">
  $white: #fff;
  $maincolor: #c0d9d3;

  .box {
    position: relative;
    padding: 20px 40px 40px;
    margin: 140px 0;
    background-color: $white;

    &::before {
      position: absolute;
      top: 0;
      left: 0;
      content: "";
      display: block;
      width: 100%;
      height: 10px;
      background-color: $maincolor;
    }

    >:first-child {
      margin-top: 0;
    }

    >:last-child {
      margin-bottom: 0;
    }

    .box__title {
      position: relative;
      margin-top: -1.6em;
      ;
      z-index: 2;
    }
  }

/* スマホ */
  @media screen and (max-width: 520px) {
    .box {
      padding: 10px 20px 20px;
      margin: 100px 0;

      .box__title {
        margin-top: -1.4em;
      }
    }
  }
</style>
