<script setup lang="ts">
  import MobileGameDemo from './MobileGameDemo.vue'
  import data from './config/mobile-demo/contents.json'
</script>

<template>
  <section class="box">
    <h2 class="headingL box__title">Demo List</h2>
    <div class="demo-content-list">
      <div v-for="item in data.contents" class="demo-content">
        <MobileGameDemo
          :createdate="item.createdate"
          :title="item.title"
          :video="item.video"
          :text="item.text"
          :demo="item.demo"
          :codes="item.codes"
        />
      </div>
    </div>
  </section>
</template>

<style lang="scss">
  .demo-content-list {

  }
  .demo-content {
    width: 100%;
    padding: 10px 0px;
  }
  /* PC */
  @media screen and (min-width: 1025px) {
    .demo-content-list {
    }
    .demo-content {
      display: inline-block;
      width: 50%;
      height: 940px;
      padding: 20px;
    }
  }
</style>
