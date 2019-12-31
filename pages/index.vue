<template>
  <div class="container">
    <div class="profiles" v-if="isActive === false">
      <div class="signboards" v-on:click="toggle_switch()">
        <div class="sign">作った物&実績</div>
        <div class="strings"></div>
        <div class="pin top"></div>
        <div class="pin left"></div>
        <div class="pin right"></div>
      </div>
      <div class="profiles__profile">
        <img src="~/assets/images/ao.png" class="profiles__profile__logo" />
        <img src="~/assets/images/name.png" class="profiles__profile__name" />
        <h2 class="profiles__profile__subtitle">
          趣味でフロントエンドを主軸にWeb技術を学んでいます。+ 絵描き🎨
        </h2>
        <dev class="profiles__profile__links">
          <a
            class="profiles__profile__links__output_logo"
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
      <div class="projects-content" v-if="isActive === true">
        <div class="projects-top">
          <div class="title-create">
            <div class="title-create__text">
              作ったもの
              <div class="title-create__icon"></div>
            </div>
          </div>
          <div class="projects">
            <a
              class="projects__project"
              href="https://github.com/aocattleya/Ramen-Timer"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">
                  ラーメンタイマー
                </h4>
                <p>カップラーメンのタイマーアプリ</p>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/timer.gif"
                  alt="ramen-timer"
                  loading="lazy"
                />
                <div class="projects__project__inner__description">
                  <p>
                    GitHub<a class="star">★</a>20↑ Qiitaトレンド入り 登壇1回
                  </p>
                  <p>【言語】JavaScript（Vue.js）</p>
                  <p>【使用】Firebase, PWA, SweetAlert</p>
                </div>
              </div>
            </a>
            <a
              class="projects__project"
              href="https://github.com/aocattleya/MiniBookSearch"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">MiniBookSearch</h4>
                <p>簡易書籍管理システム</p>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/MiniBookSearch.png"
                  alt="ramen-timer"
                  loading="lazy"
                />
                <div class="projects__project__inner__description">
                  <p>
                    GitHub<a class="star">★</a>10↑ Qiitaトレンド入り 登壇1回
                  </p>
                  <p>【言語】Python（Flask）+ Vue.js</p>
                  <p>【使用】Elasticsearch, axios, WebAPI</p>
                </div>
              </div>
            </a>
            <a
              class="projects__project"
              href="https://github.com/aocattleya/WordCloud-Japanese"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">
                  WordCloud-Japanese
                </h4>
                <p>Mecabなしで実現するWordCloud</p>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/WordCloud.png"
                  alt="ramen-timer"
                  loading="lazy"
                />
                <div class="projects__project__inner__description">
                  <p>登壇2回</p>
                  <p>【言語】Python</p>
                  <p>【使用】WordCloud</p>
                </div>
              </div>
            </a>
            <a
              class="projects__project"
              href="https://github.com/aocattleya/illustration-OriginalCharacters"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">
                  OriginalCharacters
                </h4>
                <p>描いたオリジナルキャラクターまとめ</p>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/illustration.jpg"
                  alt="ramen-timer"
                  loading="lazy"
                />
                <div class="projects__project__inner__description">
                  <p></p>
                  <p>【使用】FireAlpaca</p>
                </div>
              </div>
            </a>
            <a
              class="projects__project"
              href="https://github.com/aocattleya/NightSky-Background"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">
                  NightSky-Background
                </h4>
                <p>星の流れる動く背景</p>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/NightSky.gif"
                  alt="ramen-timer"
                  loading="lazy"
                />
                <div class="projects__project__inner__description">
                  <p>登壇1回</p>
                  <p>【言語】CSS</p>
                  <p>【使用】FireAlpaca</p>
                </div>
              </div>
            </a>
            <a
              class="projects__project"
              href="https://github.com/aocattleya/LeisurePass"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">LeisurePass</h4>
                <p>チケット販売のECサイト</p>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/LeisurePass.png"
                  alt="ramen-timer"
                  loading="lazy"
                />
                <div class="projects__project__inner__description">
                  <p></p>
                  <p>【言語】Java（Struts2）</p>
                </div>
              </div>
            </a>
            <a
              class="projects__project"
              href="https://github.com/aocattleya/GroupChat-App"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">
                  GroupChat-App
                </h4>
                <P>グループチャットアプリ</P>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/GroupChat.gif"
                  alt="ramen-timer"
                  loading="lazy"
                />
                <div class="projects__project__inner__description">
                  <p></p>
                  <p>【言語】Ruby（Ruby on Rails）</p>
                  <p>Haml, SCSS(BEM) + jQuery(Ajax)</p>
                  <p>【使用】Nginx, AWS</p>
                </div>
              </div>
            </a>
            <a
              class="projects__project"
              href="https://github.com/aocattleya/Visual_CSharpApps"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">
                  Visual_CSharpApps
                </h4>
                <p>８個のデスクトップアプリ</p>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/CSharp.jpg"
                  alt="ramen-timer"
                  loading="lazy"
                />
                <div class="projects__project__inner__description">
                  <p></p>
                  <p>【言語】C#</p>
                  <p>【使用】VisualStudio2017</p>
                </div>
              </div>
            </a>
            <a
              class="projects__project"
              href="https://github.com/aocattleya?tab=repositories"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">
                  他にも見る
                </h4>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/ripo.png"
                  alt="ramen-timer"
                  loading="lazy"
                />
                <div class="projects__project__inner__description">
                  <p>GitHubリポジトリへ</p>
                </div>
              </div>
            </a>
          </div>
          <div class="title-achievement">
            <div class="title-achievement__text">
              実績
              <div class="title-achievement__icon"></div>
            </div>
          </div>
          <div class="achievement">
            <div class="achievement__left">
              <p>受賞</p>
              <p>登壇回数</p>
              <p>GitHub</p>
              <p>Qiita</p>
              <p>ブログ</p>
            </div>
            <div class="achievement__right">
              <p>
                ：優秀新人社員賞（平成31年3月29日）<a
                  class="achievement__right__company"
                >
                  Leading Edge Co.,Ltd.</a
                >
              </p>
              <p>：3回（100名以上2回、30名以上1回）</p>
              <p>
                ：contributions1700↑ Star<a class="star">★</a>50↑ Followers120↑
              </p>
              <p>：contributions750↑ トレンド入り4回</p>
              <p>：アメーバブログで月36万PVの個人ブログの運営経験あり</p>
            </div>
          </div>
          <div class="title-other">
            <div class="title-other__text">
              Other
              <div class="title-other__icon"></div>
            </div>
          </div>
          <div class="other">
            <div class="other__text">
              <div class="other__text__left">
                <p>生年月日</p>
                <p>血液型</p>
                <p>趣味</p>
                <p>出身</p>
                <p>住み</p>
                <p>開発環境</p>
                <p>強み</p>
                <p>尊敬する人</p>
              </div>
              <div class="other__text__right">
                <p>：1993年12月7日</p>
                <p>：A型</p>
                <p>：映画、プログラミング</p>
                <p>：兵庫県 神戸市</p>
                <p>：東京都 墨田区</p>
                <p>
                  ：MacBook Pro / MacBook Air / Win10, デュアル, Corei7-7700
                </p>
                <p>
                  ：趣味でもやれて好きで取り組める事を仕事にした事、天職です。
                </p>
                <p>
                  ：ぐらばく（<a
                    class="other__text__right__link"
                    href="https://twitter.com/Grabacr07"
                    >@Grabacr07</a
                  >）さん<br />&nbsp;&nbsp;プログラミングを始めたきっかけであり目標です。
                </p>
              </div>
            </div>
            <div class="other__tweet">
              <!-- 1ツイート目 -->
              <div class="other__tweet--1">
                <blockquote class="twitter-tweet" data-lang="ja">
                  <p lang="ja" dir="ltr">
                    まつもとゆきひろさんにサインしていただいて写真まで撮って貰えた😭ありがとうございます！宝物！！<a
                      href="https://t.co/R7ihbHGXIG"
                    >
                      pic.twitter.com/R7ihbHGXIG</a
                    >
                  </p>
                  &mdash; aocattleya (@aocattleya)
                  <a
                    href="https://twitter.com/aocattleya/status/1207665158010499072?ref_src=twsrc%5Etfw"
                    >2019年12月19日</a
                  >
                </blockquote>
                <script
                  async
                  src="https://platform.twitter.com/widgets.js"
                  charset="utf-8"
                ></script>
              </div>
              <!-- 2ツイート目 -->
              <div class="other__tweet--2">
                <blockquote class="twitter-tweet" data-lang="ja">
                  <p lang="ja" dir="ltr">
                    湊川 あい（<a
                      href="https://twitter.com/llminatoll?ref_src=twsrc%5Etfw"
                      >@llminatoll</a
                    >）さんにお会いしました✨<br />自分も元々漫画描いてて憧れがあったり、わかばちゃんシリーズでGitHubが大好きになって他にも沢山影響与えてくれた方なので一生の思い出です。
                    <a href="https://t.co/uyVlKBk9V3"
                      >pic.twitter.com/uyVlKBk9V3</a
                    >
                  </p>
                  &mdash; aocattleya (@aocattleya)
                  <a
                    href="https://twitter.com/aocattleya/status/1194627288979009536?ref_src=twsrc%5Etfw"
                    >2019年11月13日</a
                  >
                </blockquote>
                <script
                  async
                  src="https://platform.twitter.com/widgets.js"
                  charset="utf-8"
                ></script>
              </div>
            </div>
            <center>
              <div class="speakerdeck">
                <script
                  async
                  class="speakerdeck-embed"
                  data-id="e0d151ad238746c49614f8436662bab7"
                  data-ratio="1.77777777777778"
                  src="//speakerdeck.com/assets/embed.js"
                ></script>
              </div>
            </center>
          </div>

          <!-- BACKボタン -->
          <div class="back">
            <div class="back__text" v-on:click="toggle_switch()">
              BACK
            </div>
          </div>
        </div>
      </div>
    </transition>
  </div>
</template>

<style lang="scss">
* {
  font-family: font;
  margin: 0;
  padding: 0;
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
  background: url('~assets/images/aotama.png');
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
  line-height: 175px;
  text-align: center;
  font-size: 40px;
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

p {
  font-size: 14px;
}

.profiles {
  width: 100%;
  height: 100vh;
  margin-top: -40px;
  margin-bottom: -40px;
  opacity: 0;
  animation-name: anime;
  animation-duration: 0.8s;
  animation-timing-function: ease-out;
  animation-iteration-count: 1;
  animation-direction: normal;
  animation-fill-mode: forwards;
  @keyframes anime {
    0% {
      opacity: 0;
      transform: translate3d(0, -20px, 0);
    }
    100% {
      opacity: 1;
      transform: translate3d(0, 0, 0);
    }
  }
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
      width: 670px;
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

.projects-content {
  border: solid 5px #283c5f;
  width: 94%;
  height: 90%;
  border-radius: 1em;
  left: calc(50% - 47%);
  top: calc(50% - 45%);
  padding-top: 40px;
  padding-bottom: 40px;
  border: solid 5px #283c5f;
  margin: 0 auto;
  background-color: white;
}

@mixin title {
  width: 500px;
  height: 80px;
  margin: 0 auto;
  margin-bottom: 50px;
  box-sizing: border-box;
  padding-top: 18px;
  position: relative;
  &::before {
    content: '';
    position: absolute;
    border: solid 2px #283c5f;
    width: 500px;
    height: 80px;
    margin: 0 auto;
    margin-bottom: 50px;
    box-sizing: border-box;
    padding-top: 18px;
    top: 4px;
    left: 4px;
  }
  &::after {
    content: '';
    position: absolute;
    border: solid 2px #283c5f;
    width: 500px;
    height: 80px;
    margin: 0 auto;
    margin-bottom: 50px;
    box-sizing: border-box;
    padding-top: 18px;
    top: -4px;
    left: -4px;
  }
  &__text {
    font-size: 30px;
    font-weight: bold;
    font-style: normal;
  }
}

.title-create {
  @include title;
  .title-create__icon {
    display: block;
    position: absolute;
    background-image: url('~@/assets/images/menma.png');
    width: 120px;
    height: 120px;
    z-index: 10;
    right: -35px;
    top: -20px;
    background-size: contain;
    background-position: center;
    background-repeat: no-repeat;
    border: none;
  }
}

.title-achievement {
  @include title;
  margin-top: 150px;
  .title-achievement__icon {
    display: block;
    position: absolute;
    background-image: url('~@/assets/images/ao.png');
    width: 120px;
    height: 120px;
    z-index: 10;
    left: -40px;
    top: -20px;
    background-size: contain;
    background-position: center;
    background-repeat: no-repeat;
    border: none;
    border-radius: 50%;
    border: solid 2px;
  }
}

.title-other {
  @include title;
  margin-top: 150px;
  .title-other__icon {
    display: block;
    position: absolute;
    background-image: url('~@/assets/images/ao2.png');
    width: 120px;
    height: 120px;
    z-index: 10;
    right: -35px;
    top: -20px;
    background-size: contain;
    background-position: center;
    background-repeat: no-repeat;
    border: none;
    border-radius: 50%;
    border: solid 2px;
  }
}

.projects {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  &__project {
    color: #35495e;
    box-shadow: 2px 2px 2px #555;
    font-size: 40px;
    margin: 30px 15px 30px;
    width: 320px;
    border: double 2px #283c5f;
    border-radius: 0.5em;
    text-decoration: none;
    transition: opacity 1s ease 0s;
    position: relative;
    &__inner {
      position: relative;
      margin-top: -45px;
      &__img {
        padding-top: 10px;
        width: calc(100% - 40px);
        height: 150px;
      }
      &__title {
        font-size: 20px;
      }
      &__description {
        margin: 0 auto;
        width: 95%;
        font-size: 15px;
        margin-bottom: 20px;
        text-align: left;
        padding: 0 10px;
        & p:nth-child(1) {
          text-align: center;
          margin-bottom: 5px;
          font-size: 13px;
          font-weight: bold;
        }
        .star {
          -webkit-text-stroke: 0.5px black;
          color: #f9f921;
          padding: 0 0.5px 0 1px;
          font-size: 12px;
        }
      }
    }
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
      background-image: url('~@/assets/images/firealpaca.png');
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
    &:nth-child(6):before {
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
      width: 60px;
      height: 60px;
      z-index: 10;
      left: -30px;
      top: -20px;
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
    }
  }
}

.achievement {
  width: 60%;
  margin: 0 auto;
  border: double 1px #283c5f;
  border-radius: 10px;
  padding: 40px 60px 40px 130px;
  text-align: left;
  display: flex;
  justify-content: center;
  &__left {
    font-size: 17px;
    p {
      margin-bottom: 15px;
    }
  }
  &__right {
    font-size: 17px;
    p {
      margin-bottom: 15px;
    }
    &__company {
      font-size: 12px;
    }
    .star {
      -webkit-text-stroke: 0.5px black;
      color: #f9f921;
      padding: 0 0.5px 2px 2px;
      font-size: 12px;
    }
  }
}

.other {
  width: 60%;
  margin: 0 auto;
  border: double 1px #283c5f;
  border-radius: 10px;
  text-align: left;
  &__text {
    margin-top: 40px;
    display: flex;
    justify-content: center;
    &__left {
      font-size: 17px;
      p {
        margin-bottom: 15px;
      }
    }
    &__right {
      font-size: 17px;
      p {
        margin-bottom: 15px;
      }
      &__link {
        color: #0099e8;
        text-decoration: none;
        &:hover {
          opacity: 0.7;
          text-decoration: underline;
        }
      }
    }
  }
  &__tweet {
    display: flex;
    justify-content: center;
    margin: 50px 0 30px;
    &--1 {
      width: 300px;
      margin-right: 20px;
    }
    &--2 {
      width: 300px;
    }
  }
}

.speakerdeck {
  max-width: 77%;
  margin: 40px;
}

.back {
  text-align: center;
  position: relative;
  text-decoration: none;
  color: #1b1b1b;
  background: #fff;
  border: 2px solid #1b1b1b;
  font-size: 20px;
  line-height: 50px;
  width: 60%;
  margin: 100px auto 30px;
  padding: 10px;
  border-radius: 5px;
  transition: 0.4s;
}

.back:hover {
  background: #1b1b1b;
  color: #fff;
  cursor: pointer;
  text-decoration: none;
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
