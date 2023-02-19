<script setup lang="ts">
import Top from './components/Top.vue'
</script>

<template> 
  <main class="mainwrapper">
    <Top />
  </main>

  
</template>

<style lang="scss">
  @charset "UTF-8";
  @import url('https://fonts.googleapis.com/css2?family=Oooh+Baby&display=swap');

  $fontcolor: #333;
  $maincolor: #c0d9d3;
  $subcolor: #ffee7c;
  $basecolor: rgba(#faf4e8, 0.3);
  $white: #fff;
  $black: #000;
  $twi: #1DA1F2;
  $insta: #CF2E92;
  $facebook: #4267b2;
  $tumblr: #39475D;
  $youtube: #DA1725;

  $fontfamily: 'Zen Kaku Gothic New', YuGothic, 'Yu Gothic medium', 'Hiragino Sans', Meiryo, 'sans-serif';
  $headingfont: 'Oooh Baby', 'Zen Kaku Gothic New', YuGothic, 'Yu Gothic medium', 'Hiragino Sans', Meiryo, 'sans-serif';

  html {
    font-size: 62.5%;
    scroll-behavior: smooth;
  }

  body {
    font-family: $fontfamily;
    font-size: 1.6rem;
    color: $fontcolor;
    letter-spacing: 2px;
    line-height: 1.8;
    background-color: $basecolor;

    @media screen and (max-width: 520px) {
      font-size: 1.4rem;
    }

    &::before,
    &::after {
      position: fixed;
      left: 0;
      content: "";
      display: block;
      width: 100%;
      height: 20px;
      background-image: linear-gradient(90deg, $maincolor 30%, $subcolor);
      z-index: 3;
    }

    &::before {
      top: 0;
    }

    &::after {
      bottom: 0;
    }
  }

  .mainwrapper {
    padding: 60px 10px;
    >:first-child {
      margin-top: 0;
    }
  }

  /* PC */
  @media screen and (min-width: 1025px),
  print {
    .mainwrapper {
      max-width: 800px;
      margin: 0 auto;
      padding: 80px 20px;
    }
  }

  p {
    margin: 20px 0;
    letter-spacing: 1px;
    text-align: justify;
  }

  a {
    color: inherit;
  }

/*－－－－－－－－－－ 見出し －－－－－－－－－－*/

  h1,
  h2,
  h3,
  h4,
  h5 {
    font-family: $headingfont;
    font-weight: normal;
    letter-spacing: 4px;
    text-align: center;
    text-transform: uppercase;
    word-break: break-all
  }

/*－－－－－－－－－－ 大見出し －－－－－－－－－－*/
  .headingL {
    font-size: clamp(3rem, 4rem, 4rem);
    margin: 40px 0;
    margin: clamp(3rem, 4rem, 4rem) 0;

    &.ja {
      font-size: clamp(2.4rem, 3rem, 3.2rem);
    }
  }

/*－－－－－－－－－－ 中見出し －－－－－－－－－－*/
  .headingM {
    font-size: clamp(2.4rem, 2rem, 3rem);
    margin: clamp(2rem, 3rem, 3rem) 0;

    &.ja {
      font-size: clamp(2rem, 2rem, 2.4rem);
    }
  }

/*－－－－－－－－－－ 小見出し －－－－－－－－－－*/
  .headingS {
    font-size: clamp(2rem, 2rem, 2.2rem);
    margin: 20px 0;

    &.ja {
      font-size: clamp(1.8rem, 2rem, 2rem);
    }
  }

/*－－－－－－－－－－ 最小見出し －－－－－－－－－－*/
  .headingSS {
    font-size: clamp(1.8rem, 2rem, 2rem);
    margin: 20px 0;
  }

/*－－－－－－－－－－ 文字装飾 －－－－－－－－－－*/
  .right {
    text-align: right;
  }

  .center {
    text-align: center;
  }

  .marker {
    background: linear-gradient(transparent 60%, $maincolor 60%);
  }

  .label {
    display: block;
    margin: 20px 0;
    padding: 2px 10px;
    background-color: $subcolor;
    width: fit-content;
  }


/*－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－

アイコン等

－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－*/
  .la,
  .las,
  .lab {
    font-size: 1.2em;
    color: $maincolor;
    position: relative;
    top: 2px;
  }

/* 矢印 */
  .arrow {
    width: 20px;
    height: 20px;
    border: 2px solid $maincolor;
    border-bottom: 0;
    border-left: 0;
    transform: rotate(45deg);
    -webkit-transform: rotate(45deg);
    -moz-transform: rotate(45deg);
    -ms-transform: rotate(45deg);
    -o-transform: rotate(45deg);
  }
</style>
