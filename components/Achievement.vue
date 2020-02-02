<template>
  <div class="projects-top">
    <div class="title-create">
      <div class="title-create__text">
        作ったもの
        <div class="title-create__icon"></div>
      </div>
    </div>
    <div class="projects">
      <Project
        v-for="(project, key, name) in projects"
        :key="name"
        :url="project.url"
        :name="project.name"
        :description="project.description"
        :img="project.img"
        :alt="project.alt"
        :performance="project.performance"
        :language="project.language"
        :use="project.use"
        :delay="project.delay"
      />
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
              Qiitaデイリー1位 &amp; 総Contribution1000ありがとうございます✨<br />今年の目標がこんなに早く同時に叶うとは思いませんでした..！
              <a href="https://t.co/tTc4VDymkJ">pic.twitter.com/tTc4VDymkJ</a>
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
              <a href="https://t.co/uyVlKBk9V3">pic.twitter.com/uyVlKBk9V3</a>
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
</template>

<style lang="scss">
@import '~assets/style/_mixins.scss';

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
import Project from '@/components/Project.vue'
export default {
  components: {
    Project
  },
  data() {
    return {
      projects: [
        {
          url: 'https://github.com/aocattleya/Ramen-Timer',
          name: 'ラーメンタイマー',
          description: 'カップラーメンのタイマーアプリ',
          img: require('@/assets/images/timer.gif'),
          alt: 'ramen-timer',
          performance: 'GitHub★45↑ Qiitaトレンド入り 登壇1回',
          language: '【言語】JavaScript（Vue.js）',
          use: '【使用】Firebase, PWA, SweetAlert',
          delay: 'animation-delay: 0.4s;'
        },
        {
          url: 'https://github.com/aocattleya/MiniBookSearch',
          name: 'MiniBookSearch',
          description: '簡易書籍管理システム',
          img: require('@/assets/images/MiniBookSearch.png'),
          alt: 'MiniBookSearch',
          performance: 'GitHub★15↑ Qiitaトレンド入り 登壇1回',
          language: '【言語】Python（Flask）+ Vue.js',
          use: '【使用】Elasticsearch, axios, WebAPI',
          delay: 'animation-delay: 0.5s;'
        },
        {
          url: 'https://github.com/aocattleya/WordCloud-Japanese',
          name: 'WordCloud-Japanese',
          description: 'Mecabなしで実現するWordCloud',
          img: require('@/assets/images/WordCloud.png'),
          alt: 'WordCloud',
          performance: '登壇2回',
          language: '【言語】Python',
          use: '【使用】WordCloud',
          delay: 'animation-delay: 0.6s;'
        },
        {
          url: 'https://github.com/aocattleya/illustration-OriginalCharacters',
          name: 'OriginalCharacters',
          description: '描いたオリジナルキャラクターまとめ',
          img: require('@/assets/images/illustration.jpg'),
          alt: 'OriginalCharacters',
          performance: '',
          language: '【使用】FireAlpaca',
          use: '【詳細】「aocattleya」と「くりんちゃん」がいます。',
          delay: 'animation-delay: 0.7s;'
        },
        {
          url: 'https://github.com/aocattleya/LeisurePass',
          name: 'LeisurePass！',
          description: 'チケット販売のECサイト',
          img: require('@/assets/images/LeisurePass.png'),
          alt: 'LeisurePass！',
          performance: '',
          language: '【言語】Java（Apache Struts2）',
          use: '【使用】Eclipse',
          delay: 'animation-delay: 0.8s;'
        },
        {
          url: 'https://github.com/aocattleya/NightSky-Background',
          name: 'NightSky-Background',
          description: '星の流れる動く背景',
          img: require('@/assets/images/NightSky.gif'),
          alt: 'NightSky-Background',
          performance: '登壇1回',
          language: '【言語】CSS',
          use: '【使用】FireAlpaca',
          delay: 'animation-delay: 0.9s;'
        },
        {
          url: 'https://github.com/aocattleya/GroupChat-App',
          name: 'GroupChat App',
          description: 'グループチャットアプリ',
          img: require('@/assets/images/GroupChat.gif'),
          alt: 'GroupChatApp',
          performance: '',
          language:
            '【言語】Ruby（Ruby on Rails） + Haml, SCSS(BEM) + jQuery(Ajax)',
          use: '【使用】AWS, Nginx',
          delay: 'animation-delay: 1s;'
        },
        {
          url: 'https://github.com/aocattleya/Mercari_clone',
          name: 'Mercari clone',
          description: 'メルカリのクローンサイト',
          img: require('@/assets/images/mercari.png'),
          alt: 'Mercari',
          performance: '登壇1回',
          language: '【言語】Ruby（Ruby on Rails）+ Haml, SCSS(BEM) + jQuery',
          use: '【使用】AWS, Nginx, OmniAuth, PAY.JP',
          delay: 'animation-delay: 1.1s;'
        },
        {
          url: 'https://github.com/aocattleya/Vue-FormValidation',
          name: 'Vue FormValidation',
          description: 'Vue CLIでフォームバリデーション',
          img: require('@/assets/images/FormValidation.gif'),
          alt: 'VueFormValidation',
          performance: '',
          language: '【言語】JavaScript（Vue.js）',
          use: '【使用】SweetAlert',
          delay: 'animation-delay: 1.2s;'
        },
        {
          url: 'https://github.com/aocattleya/Visual_CSharpApps',
          name: 'VisualC# Apps',
          description: '８個のデスクトップアプリ',
          img: require('@/assets/images/CSharp.jpg'),
          alt: 'VisualC#Apps',
          performance: '',
          language: '【言語】C#',
          use: '【使用】VisualStudio2017, WinForms, CoreTweet',
          delay: 'animation-delay: 1.3s;'
        },
        {
          url: 'https://github.com/aocattleya/Portfolio',
          name: 'Portfolio',
          description: 'Nuxt.jsでポートフォリオ',
          img: require('@/assets/images/aocattleyaSite.gif'),
          alt: 'Portfolio',
          performance: '登壇1回',
          language: '【言語】JavaScript（Nuxt.js）',
          use: '【使用】Animate.css, Firebase',
          delay: 'animation-delay: 1.4s;'
        },
        {
          url: 'https://github.com/aocattleya/Totoro-Layer',
          name: 'Totoro-Layer',
          description: 'トトロのアニメーション',
          img: require('@/assets/images/totoro.png'),
          alt: 'ramen-timer',
          performance: '',
          language: '【使用】FireAlpaca',
          use:
            '【詳細】社内忘年会のビンゴゲーム待機画面用に描かせて頂いた動くトトロ。',
          delay: 'animation-delay: 1.5s;'
        },
        {
          url: 'https://github.com/aocattleya?tab=repositories',
          name: '他にも見る',
          description: '',
          img: require('@/assets/images/kurin-github.png'),
          alt: 'other',
          performance: '現在、40個以上のリポジトリがあります。',
          language: '',
          use:
            '全てのリポジトリにデモ画像などを充実させているので是非楽しんでください。',
          delay: 'animation-delay: 1.6s;'
        }
      ],
      isActive: false
    }
  },
  methods: {
    toggleSwitch() {
      this.isActive = false
      this.$emit('profile-open', this.isActive)
    },
    hingeReturn() {
      if (this.hinge === false) {
        this.hinge = true
      } else {
        this.hinge = false
      }
    }
  }
}
</script>
