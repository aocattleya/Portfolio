<template>
  <a
    v-bind:href="url"
    class="projects__project"
    target="_blank"
    rel="noopener noreferrer"
  >
    <div class="projects__project__inner">
      <h4 class="projects__project__inner__title">
        {{ name }}
      </h4>
      <p>{{ description }}</p>
      <img
        v-bind:src="img"
        v-bind:alt="alt"
        class="projects__project__inner__img"
      />
      <div class="projects__project__inner__description">
        <p>
          {{ performance }}
        </p>
        <p>{{ language }}</p>
        <p>{{ use }}</p>
      </div>
    </div>
  </a>
</template>

<style lang="scss">
@import '~assets/style/_mixins.scss';

.projects {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  &__project {
    color: #35495e;
    box-shadow: 0 0px 3px #555;
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
      transition: 0.3s;
      background-color: #eee;
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
      background-image: url('~@/assets/images/nuxt.png');
    }
    &:nth-child(6):before {
      @include language_icon;
      background-image: url('~@/assets/images/lua.png');
    }
    &:nth-child(7):before {
      @include language_icon;
      background-image: url('~@/assets/images/java.png');
    }
    &:nth-child(8):before {
      @include language_icon;
      background-image: url('~@/assets/images/bf.png');
      border-radius: 50%;
    }
    &:nth-child(9):before {
      @include language_icon;
      background-image: url('~@/assets/images/css.png');
    }
    &:nth-child(10):before {
      @include language_icon;
      background-image: url('~@/assets/images/css.png');
      border-radius: 50%;
    }
    &:nth-child(11):before {
      @include language_icon;
      background-image: url('~@/assets/images/ruby.png');
    }
    &:nth-child(12):before {
      @include language_icon;
      background-image: url('~@/assets/images/vue.png');
    }
    &:nth-child(13):before {
      @include language_icon;
      background-image: url('~@/assets/images/cs.png');
    }
    &:nth-child(14):before {
      @include language_icon;
      background-image: url('~@/assets/images/firealpaca.png');
    }
    &:nth-child(15):before {
      @include language_icon;
      background-image: url('~@/assets/images/github.jpg');
      border-radius: 50%;
    }
  }
}
</style>

<script>
export default {
  props: {
    url: {
      type: String,
      default: 'https://github.com/aocattleya'
    },
    name: {
      type: String,
      default: 'プロジェクト'
    },
    description: {
      type: String,
      default: '説明'
    },
    img: {
      type: String,
      default: require('@/assets/images/kurin-github.png')
    },
    alt: {
      type: String,
      default: 'alt'
    },
    performance: {
      type: String,
      default: '実績'
    },
    language: {
      type: String,
      default: '言語'
    },
    use: {
      type: String,
      default: '使用'
    }
  }
}
</script>
