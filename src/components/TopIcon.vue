<template>
  <!-- プロフィール画像 -->
  <div class="profile__img"><img src="http://placehold.jp/400x400.png?text=sample" alt=""></div>
  <!-- 名前 -->
  <h1 class="myname">Game Demo<br/>Gallery</h1>
</template>

<style lang="scss">
  .myname {
    font-size: clamp(3rem, 6rem, 6rem);
    margin-top: -1.6em;
  }

  .profile__img {
    padding: 0 40px;

    img {
      border-radius: 50%;
      -webkit-border-radius: 50%;
      -moz-border-radius: 50%;
      -ms-border-radius: 50%;
      -o-border-radius: 50%;
      margin: auto;
    }
  }
</style>
