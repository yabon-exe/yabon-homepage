<script setup lang="ts">
defineProps<{
  title: string,
  video: string,
  text: string,
  demo: string,
  code: string,
  codes: {
    id: number,
    name: string,
    url: string
  }[]
}>()
</script>

<template>
  <table class="mobile-demo">
    <tr>
      <th colspan="2" class="title">
        {{title}}
      </th>
    </tr>
    <tr>
      <td colspan="2">
        <div class="video-content">
          <div class="video">
            <video controls :src="video"/>
          </div>
          <div class="text">
            {{text}}
          </div>
        </div>
      </td>
    </tr>
    <tr>
      <td class="demo-link">
        <a :href="demo" target="_blank">デモページ</a>
      </td>
      <td class="git-link">
        <a :href="codedata.url" target="_blank" v-for="codedata in codes">
          {{codedata.name}}
        </a>
      </td>
    </tr>
  </table>
</template>

<style lang="scss">
  .mobile-demo {
    width: 100%;
    video {
      max-width: 100%;
      max-height: 100%;
    }
    .title {
      font-size: 5vw;
    }
    .video-content {
      .video {

      }
      .text {

      }
    }
    .demo-link {
      text-align: center;
      width: 50%;
    }
    .git-link {
      text-align: center;
      width: 50%;
      a {
        margin: 0 10px;
        display: inline-block;
        text-overflow: ellipsis;
        overflow: hidden;
        white-space: nowrap;
        width: 100px;
      }
    }
  }
  /* PC */
  @media screen and (min-width: 1025px) {
    .mobile-demo {
      .title {
        font-size: 3vw;
      }
      .video-content {
        display: flex;
      }
      .text {
        padding: 10px;
      }
    }
  }
</style>
