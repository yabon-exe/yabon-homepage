<template>
  <section class="box">
    <h2 class="headingL box__title">About me</h2>
    <p>　ここでは、ゲーム制作に活用できそうなデモと、そのプログラムを掲載しています。
    「この動きを自分の作品に組み込みたい！」というときに、ご活用ください。</p>
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
