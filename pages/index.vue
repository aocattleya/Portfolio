<template>
  <div :class="{ hinge: bom }" class="container animated">
    <div v-if="isActive === false" class="profiles">
      <SignBoard v-on:click.native="toggleSwitch()" v-if="bomCount <= 9" />
      <Profile @bom-event="bomLargeFrame" />
    </div>
    <transition appear>
      <div v-if="isActive === true" class="projects-content">
        <Achievement @profile-open="profileOpen" />
      </div>
    </transition>
  </div>
</template>

<style lang="scss">
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
</style>

<script>
import Profile from '@/components/Profile.vue'
import Achievement from '@/components/Achievement.vue'
import SignBoard from '@/components/SignBoard.vue'
export default {
  components: {
    Profile,
    Achievement,
    SignBoard
  },
  data() {
    return {
      bomCount: null,
      bom: false,
      signboardMsg: '作った物&実績',
      isActive: false
    }
  },
  methods: {
    toggleSwitch() {
      this.isActive = true
    },
    hingeReturn() {
      if (this.hinge === false) {
        this.hinge = true
      } else {
        this.hinge = false
      }
    },
    bomLargeFrame(bomCount) {
      this.bomCount = bomCount
      if (bomCount === 10) {
        setTimeout(
          function() {
            this.bom = true
          }.bind(this),
          6500
        )
      }
    },
    profileOpen(isActive) {
      this.isActive = isActive
    }
  }
}
</script>
