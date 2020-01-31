<template>
  <div :class="{ hinge: bom }" class="container animated">
    <div v-if="isActive === false" class="profiles">
      <div
        :class="{ hinge: bom1, signboard: signboard }"
        v-on:click="toggleSwitch()"
      >
        <div :class="{ hinge: bom2, sign: sign }">{{ signboardMsg }}</div>
        <div :class="{ hinge: bom2, strings: strings }"></div>
        <div :class="{ hinge: bom2, pin: pin, top: top }"></div>
        <div :class="{ hinge: bom2, pin: pin, left: left }"></div>
        <div :class="{ hinge: bom2, pin: pin, right: right }"></div>
      </div>
      <div class="profiles__profile animated fadeIn">
        <img
          v-on:click=";(rubberBand = !rubberBand), (jello = !jello), collapse()"
          :class="{
            rubberBand: rubberBand,
            jello: jello,
            bounceOutUp: bom1
          }"
          :src="imageSrc"
          class="profiles__profile__logo animated"
        />
        <img
          :class="{ hinge: bom3 }"
          src="~/assets/images/name.png"
          class="profiles__profile__name animated"
        />
        <h2
          :class="{ hinge: bom4 }"
          class="profiles__profile__subtitle animated"
        >
          {{ description }}
        </h2>
        <div :class="{ hinge: bom5 }" class="profiles__profile__links animated">
          <a
            :class="{ hinge: bom6 }"
            class="profiles__profile__links__output_logo animated flipInX"
            href="https://connpass.com/user/aocattleya/"
            target="_blank"
            rel="noopener noreferrer"
          >
          </a>
          <a
            :class="{ hinge: bom7 }"
            class="profiles__profile__links__output_logo animated flipInX"
            href="https://qiita.com/aocattleya"
            target="_blank"
            rel="noopener noreferrer"
          ></a>
          <a
            :class="{ hinge: bom8 }"
            class="profiles__profile__links__output_logo animated flipInX"
            href="https://github.com/aocattleya"
            target="_blank"
            rel="noopener noreferrer"
          ></a>
          <a
            :class="{ hinge: bom9 }"
            class="profiles__profile__links__output_logo animated flipInX"
            href="https://twitter.com/aocattleya"
            target="_blank"
            rel="noopener noreferrer"
          ></a>
          <a
            :class="{ hinge: bom10 }"
            class="profiles__profile__links__output_logo animated flipInX"
            href="https://lapras.com/public/QIOCQBE"
            target="_blank"
            rel="noopener noreferrer"
          ></a>
        </div>
      </div>
    </div>
    <transition appear>
      <div v-if="isActive === true" class="projects-content">
        <div class="projects-top">
          <div class="title-create">
            <div class="title-create__text">
              作ったもの
              <div class="title-create__icon"></div>
            </div>
          </div>
          <div class="projects">
            <!-- ラーメンタイマー -->
            <a
              class="projects__project animated fadeInLeft"
              style="animation-delay: 0.4s;"
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
                />
                <div class="projects__project__inner__description">
                  <p>
                    GitHub<a class="star">★</a>45↑ Qiitaトレンド入り 登壇1回
                  </p>
                  <p>【言語】JavaScript（Vue.js）</p>
                  <p>【使用】Firebase, PWA, SweetAlert</p>
                </div>
              </div>
            </a>
            <!-- 簡易書籍管理システム -->
            <a
              class="projects__project animated fadeInLeft"
              style="animation-delay: 0.5s;"
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
                />
                <div class="projects__project__inner__description">
                  <p>
                    GitHub<a class="star">★</a>15↑ Qiitaトレンド入り 登壇1回
                  </p>
                  <p>【言語】Python（Flask）+ Vue.js</p>
                  <p>【使用】Elasticsearch, axios, WebAPI</p>
                </div>
              </div>
            </a>
            <!-- WordCloud-Japanese -->
            <a
              class="projects__project animated fadeInLeft"
              style="animation-delay: 0.6s;"
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
                />
                <div class="projects__project__inner__description">
                  <p>登壇2回</p>
                  <p>【言語】Python</p>
                  <p>【使用】WordCloud</p>
                </div>
              </div>
            </a>
            <!-- OriginalCharacters -->
            <a
              class="projects__project animated fadeInLeft"
              style="animation-delay: 0.7s;"
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
                />
                <div class="projects__project__inner__description">
                  <p></p>
                  <p>【使用】FireAlpaca</p>
                  <p>【詳細】「aocattleya」と「くりんちゃん」がいます。</p>
                </div>
              </div>
            </a>
            <!-- LeisurePass -->
            <a
              class="projects__project animated fadeInLeft"
              style="animation-delay: 0.8s;"
              href="https://github.com/aocattleya/LeisurePass"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">LeisurePass！</h4>
                <p>チケット販売のECサイト</p>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/LeisurePass.png"
                  alt="ramen-timer"
                />
                <div class="projects__project__inner__description">
                  <p></p>
                  <p>【言語】Java（Apache Struts2）</p>
                </div>
              </div>
            </a>
            <!-- NightSky-Background -->
            <a
              class="projects__project animated fadeInLeft"
              style="animation-delay: 0.9s;"
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
                />
                <div class="projects__project__inner__description">
                  <p>登壇1回</p>
                  <p>【言語】CSS</p>
                  <p>【使用】FireAlpaca</p>
                </div>
              </div>
            </a>
            <!-- グループチャットアプリ -->
            <a
              class="projects__project animated fadeInLeft"
              style="animation-delay: 1s;"
              href="https://github.com/aocattleya/GroupChat-App"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">
                  GroupChat App
                </h4>
                <P>グループチャットアプリ</P>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/GroupChat.gif"
                  alt="ramen-timer"
                />
                <div class="projects__project__inner__description">
                  <p></p>
                  <p>【言語】Ruby（Ruby on Rails）</p>
                  <p>Haml, SCSS(BEM) + jQuery(Ajax)</p>
                  <p>【使用】AWS, Nginx</p>
                </div>
              </div>
            </a>
            <!-- メルカリ -->
            <a
              class="projects__project animated fadeInLeft"
              style="animation-delay: 1.1s;"
              href="https://github.com/aocattleya/Mercari_clone"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">
                  Mercari clone
                </h4>
                <P>メルカリのクローンサイト</P>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/mercari.png"
                  alt="ramen-timer"
                />
                <div class="projects__project__inner__description">
                  <p>登壇1回</p>
                  <p>【言語】Ruby（Ruby on Rails）</p>
                  <p>Haml, SCSS(BEM) + jQuery</p>
                  <p>【使用】AWS, Nginx, OmniAuth, PAY.JP</p>
                </div>
              </div>
            </a>
            <!-- Vue-FormValidation -->
            <a
              class="projects__project animated fadeInLeft"
              style="animation-delay: 1.2s;"
              href="https://github.com/aocattleya/Vue-FormValidation"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">
                  Vue FormValidation
                </h4>
                <p>Vue CLIでフォームバリデーション</p>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/FormValidation.gif"
                  alt="ramen-timer"
                />
                <div class="projects__project__inner__description">
                  <p></p>
                  <p>【言語】JavaScript（Vue.js）</p>
                  <p>【使用】SweetAlert</p>
                </div>
              </div>
            </a>
            <!-- ディスクトップアプリ -->
            <a
              class="projects__project animated fadeInLeft"
              style="animation-delay: 1.3s;"
              href="https://github.com/aocattleya/Visual_CSharpApps"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">
                  VisualC# Apps
                </h4>
                <p>８個のデスクトップアプリ</p>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/CSharp.jpg"
                  alt="ramen-timer"
                />
                <div class="projects__project__inner__description">
                  <p></p>
                  <p>【言語】C#</p>
                  <p>【使用】VisualStudio2017<br />WindowsForms, CoreTweet</p>
                </div>
              </div>
            </a>
            <!-- Portfolio -->
            <a
              class="projects__project animated fadeInLeft"
              style="animation-delay: 1.4s;"
              href="https://github.com/aocattleya/Portfolio"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">
                  Portfolio
                </h4>
                <p>Nuxt.jsでポートフォリオ</p>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/aocattleyaSite.gif"
                  alt="ramen-timer"
                />
                <div class="projects__project__inner__description">
                  <p>登壇1回</p>
                  <p>【言語】JavaScript（Nuxt.js）</p>
                  <p>【使用】Animate.css, Firebase</p>
                </div>
              </div>
            </a>
            <!-- Totoro-Layer -->
            <a
              class="projects__project animated fadeInLeft"
              style="animation-delay: 1.5s;"
              href="https://github.com/aocattleya/Totoro-Layer"
              target="_blank"
              rel="noopener noreferrer"
            >
              <div class="projects__project__inner">
                <h4 class="projects__project__inner__title">
                  Totoro-Layer
                </h4>
                <p>トトロのアニメーション</p>
                <img
                  class="projects__project__inner__img"
                  src="~assets/images/totoro.png"
                  alt="ramen-timer"
                />
                <div class="projects__project__inner__description">
                  <p></p>
                  <p>【使用】FireAlpaca</p>
                  <p>
                    【詳細】社内忘年会のビンゴゲーム待機画面用に描かせて頂いた動くトトロ。
                  </p>
                </div>
              </div>
            </a>
            <!-- 他 -->
            <a
              class="projects__project animated fadeInLeft"
              style="animation-delay: 1.6s;"
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
                  src="~assets/images/kurin-github.png"
                  alt="ramen-timer"
                />
                <div class="projects__project__inner__description">
                  <p>現在、40個以上のリポジトリがあります。</p>
                  <p>
                    全てのリポジトリにデモ画像などを充実させているので是非楽しんでください。
                  </p>
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
                  class="achievement__right--company"
                >
                  Leading Edge Co.,Ltd.</a
                >
              </p>
              <p>：4回（100名以上2回、70名以上1回、30名以上1回）</p>
              <p>
                ：Contributions2000↑ Star90↑ Followers150↑
              </p>
              <p>：Contributions1700↑ トレンド入り5回</p>
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
              <div class="other__tweet--1">
                <!-- 1ツイート目 -->
                <blockquote class="twitter-tweet" data-lang="ja">
                  <p lang="ja" dir="ltr">
                    Qiitaデイリー1位 &amp;
                    総Contribution1000ありがとうございます✨<br />今年の目標がこんなに早く同時に叶うとは思いませんでした..！
                    <a href="https://t.co/tTc4VDymkJ"
                      >pic.twitter.com/tTc4VDymkJ</a
                    >
                  </p>
                  &mdash; aocattleya (@aocattleya)
                  <a
                    href="https://twitter.com/aocattleya/status/1215780083023011840?ref_src=twsrc%5Etfw"
                    >2020年1月10日</a
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
              <!-- 3ツイート目 -->
              <div class="other__tweet--3">
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
            <div class="speakerdeck">
              <script
                async
                class="speakerdeck-embed"
                data-id="e0d151ad238746c49614f8436662bab7"
                data-ratio="1.77777777777778"
                src="//speakerdeck.com/assets/embed.js"
              ></script>
            </div>
          </div>
          <!-- BACKボタン -->
          <div v-on:click="toggleSwitch(), hingeReturn()" class="back">
            <div class="back__text">
              <b>TOP</b>
              <span>（TOPのキャラクターロゴを10回押すと・・・？）</span>
            </div>
          </div>
        </div>
      </div>
    </transition>
  </div>
</template>

<style lang="scss">
@import '~assets/style/_signboard.scss';
@import '~assets/style/_mixins.scss';

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
      animation-delay: 2.5s;
      border-radius: 50%;
      width: 200px;
      display: block;
      margin: 0 auto;
      cursor: pointer;
    }
    &__name {
      background: url('~assets/images/name.png');
      width: 400px;
      margin-bottom: 20px;
    }
    &__subtitle {
      font-size: 20px;
      color: #526488;
      word-spacing: 5px;
      margin-top: 20px;
      font-weight: 300;
      margin-bottom: 10px;
      display: block;
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
        background: url('~assets/images/connpass.png');
        width: 110px;
        height: 110px;
        margin-top: 10px;
        animation-delay: 0.4s;
        @include output_logo;
      }
      &__output_logo:nth-child(2) {
        background: url('~assets/images/qiita.png');
        width: 120px;
        height: 120px;
        animation-delay: 0.5s;
        @include output_logo;
      }
      &__output_logo:nth-child(3) {
        background: url('~assets/images/github.jpg');
        width: 120px;
        height: 120px;
        animation-delay: 0.6s;
        @include output_logo;
      }
      &__output_logo:nth-child(4) {
        background: url('~assets/images/twitter.png');
        width: 120px;
        height: 120px;
        animation-delay: 0.7s;
        @include output_logo;
      }
      &__output_logo:nth-child(5) {
        background: url('~assets/images/lapras.jpg');
        width: 110px;
        height: 110px;
        margin-top: 10px;
        animation-delay: 0.8s;
        @include output_logo;
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

.title-create {
  @include title;
  animation-delay: 0.5s;
  .title-create__icon {
    display: block;
    position: absolute;
    background-image: url('~@/assets/images/旧aocattleya.jpg');
    width: 120px;
    height: 120px;
    z-index: 10;
    right: -35px;
    top: -20px;
    background-size: contain;
    background-position: center;
    background-repeat: no-repeat;
    border-radius: 50%;
    border: solid 2px;
  }
}

.title-achievement {
  @include title;
  margin-top: 150px;
  .title-achievement__icon {
    display: block;
    position: absolute;
    background-image: url('~@/assets/images/ao2.png');
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
    background-image: url('~@/assets/images/ao3.png');
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
      @include language_icon;
      background-image: url('~@/assets/images/vue.png');
      padding-bottom: -40px;
    }
    &:nth-child(2):before {
      @include language_icon;
      background-image: url('~@/assets/images/flask.png');
    }
    &:nth-child(3):before {
      @include language_icon;
      background-image: url('~@/assets/images/python.png');
    }
    &:nth-child(3):before {
      @include language_icon;
      background-image: url('~@/assets/images/python.png');
    }
    &:nth-child(4):before {
      @include language_icon;
      background-image: url('~@/assets/images/firealpaca.png');
    }
    &:nth-child(5):before {
      @include language_icon;
      background-image: url('~@/assets/images/java.png');
    }
    &:nth-child(6):before {
      @include language_icon;
      background-image: url('~@/assets/images/css.png');
    }
    &:nth-child(7):before {
      @include language_icon;
      background-image: url('~@/assets/images/ruby.png');
    }
    &:nth-child(8):before {
      @include language_icon;
      background-image: url('~@/assets/images/ruby.png');
      border-radius: 50%;
    }
    &:nth-child(9):before {
      @include language_icon;
      background-image: url('~@/assets/images/vue.png');
    }
    &:nth-child(10):before {
      @include language_icon;
      background-image: url('~@/assets/images/cs.png');
    }
    &:nth-child(11):before {
      @include language_icon;
      background-image: url('~@/assets/images/nuxt.png');
    }
    &:nth-child(12):before {
      @include language_icon;
      background-image: url('~@/assets/images/firealpaca.png');
    }
    &:nth-child(13):before {
      @include language_icon;
      background-image: url('~@/assets/images/github.jpg');
      border-radius: 50%;
    }
  }
}

.achievement {
  width: 60%;
  margin: 0 auto;
  border: double 1px #283c5f;
  border-radius: 10px;
  padding: 40px 60px 25px 100px;
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
  }
  &__right--company {
    font-size: 12px;
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
    justify-content: space-between;
    margin: 35px auto 30px;
    flex-wrap: wrap;
    width: 650px;
  }
  &__tweet--1 {
    margin: 0 auto;
  }
  &__tweet--2 {
    width: 310px;
  }
  &__tweet--3 {
    width: 310px;
  }
}

.speakerdeck {
  max-width: 77%;
  margin: 40px auto;
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
  &:hover {
    background: #1b1b1b;
    color: #fff;
    cursor: pointer;
    text-decoration: none;
  }
}

@media only screen and (max-width: 1000px) {
  .achievement {
    padding: 40px 30px 25px 30px;
  }
}
</style>

<script>
export default {
  data() {
    return {
      imageSrc: require('~/assets/images/aocattleya.jpg'),
      signboardMsg: '作った物&実績',
      description:
        '趣味でフロントエンドを主軸にWeb技術を学んでいます。+ 絵描き🎨',
      isActive: false,
      rubberBand: false,
      jello: true,
      pulse: false,
      bomCount: null,
      signboard: true,
      sign: true,
      strings: true,
      pin: true,
      top: true,
      left: true,
      right: true,
      bom: false,
      bom1: false,
      bom2: false,
      bom3: false,
      bom4: false,
      bom5: false,
      bom6: false,
      bom7: false,
      bom8: false,
      bom9: false,
      bom10: false
    }
  },
  methods: {
    toggleSwitch() {
      this.isActive = !this.isActive
    },
    hingeReturn() {
      if (this.hinge === false) {
        this.hinge = true
      } else {
        this.hinge = false
      }
    },
    collapse() {
      this.bomCount += 1
      if (this.bomCount === 10) {
        this.imageSrc = require('~/assets/images/aocattleyaSorrow.jpg')
        this.signboardMsg = ''
        this.jello = false
        this.signboard = false
        this.sign = false
        this.strings = false
        this.pin = false
        this.top = false
        this.left = false
        this.right = false
        setTimeout(
          function() {
            this.bom = true
          }.bind(this),
          6500
        )
        setTimeout(
          function() {
            this.bom1 = true
          }.bind(this),
          2200
        )
        setTimeout(
          function() {
            this.bom2 = true
          }.bind(this),
          1400
        )
        setTimeout(
          function() {
            this.bom3 = true
          }.bind(this),
          300
        )
        setTimeout(
          function() {
            this.bom4 = true
          }.bind(this),
          2000
        )
        setTimeout(
          function() {
            this.bom5 = true
          }.bind(this),
          5500
        )
        setTimeout(
          function() {
            this.bom6 = true
          }.bind(this),
          1800
        )
        setTimeout(
          function() {
            this.bom7 = true
          }.bind(this),
          2300
        )
        setTimeout(
          function() {
            this.bom8 = true
          }.bind(this),
          2800
        )
        setTimeout(
          function() {
            this.bom9 = true
          }.bind(this),
          1500
        )
        setTimeout(
          function() {
            this.bom10 = true
          }.bind(this),
          2500
        )
      }
    }
  }
}
</script>
