<script setup lang="ts">
import TopIcon from './TopIcon.vue'
import SectionAboutMe from './SectionAboutMe.vue'
import SectionAttention from './SectionAttention.vue'
</script>

<template>
  <TopIcon />
  <SectionAboutMe />
  <SectionAttention />
</template>

<style lang="scss">
/* セクションスタイル */
  $white: #fff;
  $maincolor: #c0d9d3;

  .box {
    position: relative;
    padding: 20px 40px 40px;
    background-color: $white;
    color: black;

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
      ;
      z-index: 2;
    }
  }

/* スマホ */
  @media screen and (max-width: 520px) {
    .box {
      padding: 10px 20px 20px;
      .box__title {
      }
    }
  }
</style>
