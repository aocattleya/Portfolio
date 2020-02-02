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
