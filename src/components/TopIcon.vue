<template>
  <!-- プロフィール画像 -->
  <div class="profile__img"><img src="/img/phone-game-demo.jpg" alt=""></div>
  <!-- 名前 -->
  <h1 class="myname">Mobile Game<br/>Demo Gallery</h1>
</template>

<style lang="scss">
  .myname {
    font-size: 8vw;
    margin-top: -2.6em
  }

  .profile__img {
    margin: auto;
    display: flex;

    img {
      border-radius: 50%;
      -webkit-border-radius: 50%;
      -moz-border-radius: 50%;
      -ms-border-radius: 50%;
      -o-border-radius: 50%;
      margin: auto;
      max-width: 100%;
    }
  }

  /* PC */
  @media screen and (min-width: 1025px) {
    .myname {
      font-size: 6vw;
      margin-top: -2.6em
    }
  }
</style>
