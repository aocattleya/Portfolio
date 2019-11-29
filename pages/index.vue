<template>
  <div class="container">
    <div class="profiles">
      <div class="profiles__profile">
        <img src="~/assets/images/ao.png" class="profiles__profile__logo" />
        <img src="~/assets/images/name.png" class="profiles__profile__name" />
        <h2 class="profiles__profile__subtitle">
          趣味でフロントエンドを主軸にWeb技術を学んでいます。+ 絵🎨
        </h2>
        <dev class="profiles__profile__links">
          <a
            class="profiles__profile__links__output_logo"
            href="https://github.com/aocattleya"
            target="_blank"
          ></a>
          <a
            class="profiles__profile__links__output_logo"
            href="https://qiita.com/aocattleya"
            target="_blank"
          ></a>
          <a
            class="profiles__profile__links__output_logo"
            href="https://twitter.com/aocattleya"
            target="_blank"
          ></a>
          <a
            class="profiles__profile__links__output_logo"
            href="https://cattleya.hatenablog.com/"
            target="_blank"
          ></a>
          <a
            class="profiles__profile__links__output_logo"
            href="https://connpass.com/user/aocattleya/"
            target="_blank"
          ></a>
        </dev>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
@mixin text {
  font-size: 20px;
  color: #526488;
  word-spacing: 5px;
  margin-top: 20px;
}

@mixin project-title {
  color: #35495e;
  font-size: 50px;
  margin-bottom: 20px;
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  justify-content: center;
  align-items: center;
  text-align: center;
  max-width: 100%;
  height: 100%;
  object-fit: cover;
}

.profiles {
  width: 100%;
  height: 100vh;
  // background-color: #fffcf4;
  background: url('~assets/images/mizutama.png');
  &__profile {
    position: absolute;
    border: dashed 5px #283c5f;
    left: calc(50% - 45%);
    top: calc(50% - 45%);
    width: 90%;
    height: 90%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: white;
    &__logo {
      border-radius: 50%;
      width: 200px;
      display: block;
      margin: 0 auto;
    }
    &__name {
      background: url('~assets/images/name.png');
      width: 400px;
      margin-bottom: 20px;
    }
    &__subtitle {
      @include text;
      font-weight: 300;
      margin-bottom: 10px;
    }
    &__links {
      width: 50%;
      margin: 0 auto;
      list-style: none;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      border-top: 1px solid rgb(141, 141, 141);
      padding-top: 20px;
      margin-bottom: 20px;
      &__output_logo {
        width: 100px;
        height: 100px;
        box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
        content: '';
        display: block;
        background-size: cover;
        background-position: center;
      }
      &__output_logo:nth-child(1) {
        width: 100px;
        height: 100px;
        margin-top: 10px;
        box-shadow: rgba(79, 194, 220, 0.2) 0px 0px 20px;
        background: url('~assets/images/connpass.png');
        background-size: cover;
        background-position: center;
      }
      &__output_logo:nth-child(2) {
        width: 110px;
        height: 110px;
        box-shadow: rgba(79, 194, 220, 0.2) 0px 0px 20px;
        background: url('~assets/images/qiita.png');
        background-size: cover;
        background-position: center;
      }
      &__output_logo:nth-child(3) {
        width: 110px;
        height: 110px;
        box-shadow: rgba(79, 194, 220, 0.2) 0px 0px 20px;
        background: url('~assets/images/github.jpg');
        background-size: cover;
        background-position: center;
      }
      &__output_logo:nth-child(4) {
        width: 110px;
        height: 110px;
        box-shadow: rgba(79, 194, 220, 0.2) 0px 0px 20px;
        background: url('~assets/images/twitter.png');
        background-size: cover;
        background-position: center;
      }
      &__output_logo:nth-child(5) {
        width: 100px;
        height: 100px;
        margin-top: 10px;
        box-shadow: rgba(79, 194, 220, 0.2) 0px 0px 20px;
        background: url('~assets/images/hatena.jpg');
        background-size: cover;
        background-position: center;
      }
    }
  }
}

.projects {
  width: 1000px;
  height: 2000px;
  background-color: #ccc;
  margin: 0 auto;
  &__project-title {
    @include project-title;
  }
  &__timer {
    &__timergif {
      width: 730px;
    }
    &__content {
      width: 650px;
      margin: 0 auto;
      background-color: aqua;
      &__text {
        @include text;
        text-align: left;
      }
    }
  }
}
</style>
