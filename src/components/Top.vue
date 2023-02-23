<script setup lang="ts">
  import BuildVersion from './BuildVersion.vue'
  import TopIcon from './TopIcon.vue'
  import SectionAboutMe from './SectionAboutMe.vue'
  import SectionAttention from './SectionAttention.vue'
  import MobileGameDemoList from './MobileGameDemoList.vue'
</script>

<template>
  <BuildVersion />
  <TopIcon />
  <SectionAboutMe />
  <SectionAttention />
  <MobileGameDemoList />
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
      z-index: 2;
    }
  }

/* スマホ */
  @media screen and (max-width: 520px) {
    .box {
      padding: 10px 20px 20px;
      margin: 30px 0px;
      .box__title {
        margin: 0px;
        margin: -35px 0px 0px 0px;
      }
    }
  }
</style>
