<template>
  <div class="container">
    <div class="profiles" v-if="isActive === false">
      <div class="signboards" v-on:click="toggle_switch()">
        <div class="sign">作った物</div>
        <div class="strings"></div>
        <div class="pin top"></div>
        <div class="pin left"></div>
        <div class="pin right"></div>
      </div>
      <div class="profiles__profile">
        <img src="~/assets/images/ao.png" class="profiles__profile__logo" />
        <img src="~/assets/images/name.png" class="profiles__profile__name" />
        <h2 class="profiles__profile__subtitle">
          趣味でフロントエンドを主軸にWeb技術を学んでいます。+ 絵🎨
        </h2>
        <dev class="profiles__profile__links">
          <a
            class="profiles__profile__links__output_logo connpass"
            href="https://connpass.com/user/aocattleya/"
            target="_blank"
            rel="noopener noreferrer"
          >
          </a>
          <a
            class="profiles__profile__links__output_logo"
            href="https://qiita.com/aocattleya"
            target="_blank"
            rel="noopener noreferrer"
          ></a>
          <a
            class="profiles__profile__links__output_logo"
            href="https://github.com/aocattleya"
            target="_blank"
            rel="noopener noreferrer"
          ></a>
          <a
            class="profiles__profile__links__output_logo"
            href="https://twitter.com/aocattleya"
            target="_blank"
            rel="noopener noreferrer"
          ></a>
          <a
            class="profiles__profile__links__output_logo"
            href="https://cattleya.hatenablog.com/"
            target="_blank"
            rel="noopener noreferrer"
          ></a>
        </dev>
      </div>
    </div>
    <transition appear>
      <div class="projects" v-if="isActive === true">
        <a
          class="projects__project"
          href="https://github.com/aocattleya/Ramen-Timer"
          target="_blank"
          rel="noopener noreferrer"
        >
          <div class="projects__project__inner">
            <img
              class="projects__project__inner__img"
              src="~assets/images/timer.gif"
              alt="ramen-timer"
              loading="lazy"
            />
            <h4 class="projects__project__inner__title">ラーメンタイマー</h4>
            <p class="projects__project__inner__description">
              カップラーメンのタイマーアプリ
            </p>
          </div>
        </a>
        <a
          class="projects__project"
          href="https://github.com/aocattleya/MiniBookSearch"
          target="_blank"
          rel="noopener noreferrer"
        >
          <div class="projects__project__inner">
            <img
              class="projects__project__inner__img"
              src="~assets/images/MiniBookSearch.png"
              alt="ramen-timer"
              loading="lazy"
            />
            <h4 class="projects__project__inner__title">MiniBookSearch</h4>
            <p class="projects__project__inner__description">
              簡易書籍管理システム
            </p>
          </div>
        </a>
        <a
          class="projects__project"
          href="https://github.com/aocattleya/WordCloud-Japanese"
          target="_blank"
          rel="noopener noreferrer"
        >
          <div class="projects__project__inner">
            <img
              class="projects__project__inner__img"
              src="~assets/images/WordCloud.png"
              alt="ramen-timer"
              loading="lazy"
            />
            <h4 class="projects__project__inner__title">WordCloud-Japanese</h4>
            <p class="projects__project__inner__description">
              Mecabなしで実現するWordCloud
            </p>
          </div>
        </a>
        <a
          class="projects__project"
          href="https://github.com/aocattleya/illustration-OriginalCharacters"
          target="_blank"
          rel="noopener noreferrer"
        >
          <div class="projects__project__inner">
            <img
              class="projects__project__inner__img"
              src="~assets/images/illustration.jpg"
              alt="ramen-timer"
              loading="lazy"
            />
            <h4 class="projects__project__inner__title">OriginalCharacters</h4>
            <p class="projects__project__inner__description">
              描いたオリジナルキャラクターまとめ
            </p>
          </div>
        </a>
        <a
          class="projects__project"
          href="https://github.com/aocattleya/LeisurePass"
          target="_blank"
          rel="noopener noreferrer"
        >
          <div class="projects__project__inner">
            <img
              class="projects__project__inner__img"
              src="~assets/images/LeisurePass.png"
              alt="ramen-timer"
              loading="lazy"
            />
            <h4 class="projects__project__inner__title">LeisurePass</h4>
            <p class="projects__project__inner__description">
              チケット販売のECサイト
            </p>
          </div>
        </a>
        <a
          class="projects__project"
          href="https://github.com/aocattleya/NightSky-Background"
          target="_blank"
          rel="noopener noreferrer"
        >
          <div class="projects__project__inner">
            <img
              class="projects__project__inner__img"
              src="~assets/images/NightSky.gif"
              alt="ramen-timer"
              loading="lazy"
            />
            <h4 class="projects__project__inner__title">NightSky-Background</h4>
            <p class="projects__project__inner__description">
              星の流れる動く背景
            </p>
          </div>
        </a>
        <a
          class="projects__project"
          href="https://github.com/aocattleya/GroupChat-App"
          target="_blank"
          rel="noopener noreferrer"
        >
          <div class="projects__project__inner">
            <img
              class="projects__project__inner__img"
              src="~assets/images/GroupChat.gif"
              alt="ramen-timer"
              loading="lazy"
            />
            <h4 class="projects__project__inner__title">GroupChat-App</h4>
            <p class="projects__project__inner__description">
              グループチャットアプリ
            </p>
          </div>
        </a>
        <a
          class="projects__project"
          href="https://github.com/aocattleya/Visual_CSharpApps"
          target="_blank"
          rel="noopener noreferrer"
        >
          <div class="projects__project__inner">
            <img
              class="projects__project__inner__img"
              src="~assets/images/CSharp.jpg"
              alt="ramen-timer"
              loading="lazy"
            />
            <h4 class="projects__project__inner__title">Visual_CSharpApps</h4>
            <p class="projects__project__inner__description">
              ８個のディスクトップアプリ
            </p>
          </div>
        </a>
        <a
          class="projects__project"
          href="https://github.com/aocattleya?tab=repositories"
          target="_blank"
          rel="noopener noreferrer"
        >
          <div class="projects__project__inner">
            <img
              class="projects__project__inner__img"
              src="~assets/images/ripo.png"
              alt="ramen-timer"
              loading="lazy"
            />
            <h4 class="projects__project__inner__title">他にも見る</h4>
            <p class="projects__project__inner__description">
              GitHubリポジトリへ
            </p>
          </div>
        </a>
      </div>
    </transition>
  </div>
</template>

<style lang="scss">
* {
  font-family: font;
}

@mixin text {
  font-size: 20px;
  color: #526488;
  word-spacing: 5px;
  margin-top: 20px;
}

$font: 'Hiragino Kaku Gothic Pro', 'ヒラギノ角ゴ Pro W3', 'メイリオ', Meiryo,
  'ＭＳ Ｐゴシック', sans-serif;

.v-enter-active {
  transition: opacity 0.8s, transform 0.7s;
}

.v-enter {
  opacity: 0;
  transform: translateY(30px);
}

.container {
  margin: 0 auto;
  height: 100%;
  padding-top: 40px;
  padding-bottom: 40px;
  justify-content: center;
  align-items: center;
  text-align: center;
  max-width: 100%;
  height: 100%;
  object-fit: cover;
  position: relative;
  background: url('~assets/images/mizutama.png');
}

.signboards {
  position: absolute;
  top: 32px;
  right: 100px;
  width: 400px;
  height: 300px;
  margin-left: 500px;
  animation: swinging 4s ease-in-out infinite alternate;
  z-index: 1;
  opacity: 1;
  cursor: pointer;
}

.signboards .sign {
  position: absolute;
  top: 100px;
  left: 38px;
  bottom: 0;
  width: 80%;
  height: 150px;
  background: burlywood;
  border-radius: 15px;
  line-height: 200px;
  text-align: center;
  font-size: 60px;
  font-weight: 700;
  font-family: sans-serif;
  color: saddlebrown;
  text-shadow: 0 2px 0 rgba(255, 255, 255, 0.3), 0 -2px 0 rgba(0, 0, 0, 0.7);
  font-family: font;
}

.strings {
  position: absolute;
  top: 38px;
  left: 125px;
  width: 150px;
  height: 150px;
  border: 5px solid brown;
  transform: rotate(45deg);
  border-right: none;
  border-bottom: none;
}

.pin {
  position: absolute;
  width: 25px;
  height: 25px;
  border-radius: 50%;
}

.pin.top {
  background: gray;
  left: calc((400px - 25px) / 2);
}

.pin.right,
.pin.left {
  background: brown;
  top: 110px;
  box-shadow: 0 2px 0 rgba(255, 255, 255, 0.3);
}

.pin.left {
  left: calc((200px - 25px) / 2);
}

.pin.right {
  left: calc(200px + (200px - 25px) / 2);
}

@keyframes swinging {
  from {
    transform: rotate(10deg) translateX(-22px);
  }
  to {
    transform: rotate(-10deg) translateX(22px);
  }
}

.profiles {
  width: 100%;
  height: 100vh;
  margin-top: -40px;
  margin-bottom: -40px;
  &__profile {
    position: absolute;
    border: solid 5px #283c5f;
    border-radius: 1em;
    left: calc(50% - 47%);
    top: calc(50% - 45%);
    width: 94%;
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
        display: block;
        width: 110px;
        height: 110px;
        margin-top: 10px;
        box-shadow: rgba(79, 194, 220, 0.2) 0px 0px 20px;
        background: url('~assets/images/connpass.png');
        background-size: cover;
        background-position: center;
      }
      &__output_logo:nth-child(2) {
        width: 120px;
        height: 120px;
        box-shadow: rgba(79, 194, 220, 0.2) 0px 0px 20px;
        background: url('~assets/images/qiita.png');
        background-size: cover;
        background-position: center;
      }
      &__output_logo:nth-child(3) {
        width: 120px;
        height: 120px;
        box-shadow: rgba(79, 194, 220, 0.2) 0px 0px 20px;
        background: url('~assets/images/github.jpg');
        background-size: cover;
        background-position: center;
      }
      &__output_logo:nth-child(4) {
        width: 120px;
        height: 120px;
        box-shadow: rgba(79, 194, 220, 0.2) 0px 0px 20px;
        background: url('~assets/images/twitter.png');
        background-size: cover;
        background-position: center;
      }
      &__output_logo:nth-child(5) {
        width: 110px;
        height: 110px;
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
  margin: 0 auto;
  background-color: white;
  border: solid 5px #283c5f;
  border-radius: 1em;
  left: calc(50% - 47%);
  top: calc(50% - 45%);
  width: 94%;
  height: 90%;
  padding-top: 40px;
  padding-bottom: 40px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  &__project {
    color: #35495e;
    box-shadow: 2px 2px 2px #555;
    font-size: 50px;
    margin-bottom: 40px;
    width: 450px;
    margin: 30px;
    border: double 2px #283c5f;
    border-radius: 0.5em;
    text-decoration: none;
    transition: opacity 1s ease 0s;
    position: relative;
    &:hover {
      box-shadow: none;
      transition: 0.5s;
    }
    &:nth-child(1):before {
      content: '';
      display: block;
      position: relative;
      background-image: url('~@/assets/images/vue.png');
      width: 60px;
      height: 60px;
      z-index: 10;
      left: -30px;
      top: -20px;
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
      padding-bottom: -40px;
    }
    &:nth-child(2):before {
      content: '';
      display: block;
      position: relative;
      background-image: url('~@/assets/images/python.png');
      width: 60px;
      height: 60px;
      z-index: 10;
      left: -30px;
      top: -20px;
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
    }
    &:nth-child(3):before {
      content: '';
      display: block;
      position: relative;
      background-image: url('~@/assets/images/python.png');
      width: 60px;
      height: 60px;
      z-index: 10;
      left: -30px;
      top: -20px;
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
    }
    &:nth-child(3):before {
      content: '';
      display: block;
      position: relative;
      background-image: url('~@/assets/images/python.png');
      width: 60px;
      height: 60px;
      z-index: 10;
      left: -30px;
      top: -20px;
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
    }
    &:nth-child(4):before {
      content: '';
      display: block;
      position: relative;
      background-image: url('~@/assets/images/FireAlpaca.jpeg');
      width: 60px;
      height: 60px;
      z-index: 10;
      left: -30px;
      top: -20px;
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
    }
    &:nth-child(5):before {
      content: '';
      display: block;
      position: relative;
      background-image: url('~@/assets/images/java.png');
      width: 60px;
      height: 60px;
      z-index: 10;
      left: -30px;
      top: -20px;
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
    }
    &:nth-child(6):before {
      content: '';
      display: block;
      position: relative;
      background-image: url('~@/assets/images/css.png');
      width: 60px;
      height: 60px;
      z-index: 10;
      left: -30px;
      top: -20px;
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
    }
    &:nth-child(7):before {
      content: '';
      display: block;
      position: relative;
      background-image: url('~@/assets/images/ruby.png');
      width: 60px;
      height: 60px;
      z-index: 10;
      left: -30px;
      top: -20px;
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
    }
    &:nth-child(8):before {
      content: '';
      display: block;
      position: relative;
      background-image: url('~@/assets/images/cs.png');
      width: 60px;
      height: 60px;
      z-index: 10;
      left: -30px;
      top: -20px;
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
    }
    &:nth-child(9):before {
      content: '';
      display: block;
      position: relative;
      background-image: url('~@/assets/images/github.jpg');
      border-radius: 50%;
      width: 65px;
      height: 65px;
      z-index: 10;
      left: -30px;
      top: -20px;
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
    }
    &__inner {
      position: relative;
      margin-top: -45px;
      &__img {
        padding-top: 10px;
        width: calc(100% - 40px);
        height: 205px;
      }
      &__title {
        font-size: 20px;
      }
      &__description {
        margin: 0 auto;
        width: 95%;
        font-size: 20px;
        margin-bottom: 20px;
      }
    }
  }
}
</style>

<script>
export default {
  data() {
    return {
      isActive: false
    }
  },
  methods: {
    toggle_switch() {
      this.isActive = !this.isActive
    }
  }
}
</script>
