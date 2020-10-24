<template>
  <div class="profiles__profile animated fadeIn">
    <img
      v-on:click=";(rubberBand = !rubberBand), (jello = !jello), collapse()"
      :class="{ rubberBand: rubberBand, jello: jello, bounceOutUp: bom5 }"
      :src="imageSrc"
      class="profiles__profile__logo animated"
      alt="aocattleya"
    />
    <img
      :class="{ hinge: bom1 }"
      src="~/assets/images/name.png"
      class="profiles__profile__name animated"
      alt=""
    />
    <h2 :class="{ hinge: bom2 }" class="profiles__profile__subtitle animated">
      {{ description }}
    </h2>
    <div :class="{ hinge: bom3 }" class="profiles__profile__links animated">
      <a
        :class="{ hinge: bom4 }"
        class="profiles__profile__links__output--connpass animated flipInX"
        href="https://connpass.com/user/aocattleya"
        target="_blank"
        rel="noopener noreferrer"
        alt="connpass"
      >
      </a>
      <a
        :class="{ hinge: bom5 }"
        class="profiles__profile__links__output--qiita animated flipInX"
        href="https://qiita.com/aocattleya"
        target="_blank"
        rel="noopener noreferrer"
        alt="qiita"
      >
      </a>
      <a
        :class="{ hinge: bom6 }"
        class="profiles__profile__links__output--github animated flipInX"
        href="https://github.com/aocattleya"
        target="_blank"
        rel="noopener noreferrer"
        alt="github"
      >
      </a>
      <a
        :class="{ hinge: bom7 }"
        class="profiles__profile__links__output--twitter animated flipInX"
        href="https://twitter.com/aocattleya"
        target="_blank"
        rel="noopener noreferrer"
        alt="twitter"
      >
      </a>
      <a
        :class="{ hinge: bom8 }"
        class="profiles__profile__links__output--lapras animated flipInX"
        href="https://lapras.com/public/QIOCQBE"
        target="_blank"
        rel="noopener noreferrer"
        alt="twitter"
      >
      </a>
    </div>
    <div v-on:click="toggleSwitch()" class="switch">作ったもの&実績</div>
  </div>
</template>

<style lang="scss">
@import '~assets/style/_mixins.scss';

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
      &__output {
        width: 100px;
        height: 100px;
        box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
        content: '';
        display: block;
        background-size: cover;
        background-position: center;
        border-style: none;
      }
      &__output--connpass {
        background: url('~assets/images/connpass.png');
        width: 110px;
        height: 110px;
        margin-top: 10px;
        animation-delay: 0.4s;
        @include output_logo;
      }
      &__output--qiita {
        background: url('~assets/images/qiita.png');
        width: 120px;
        height: 120px;
        animation-delay: 0.5s;
        @include output_logo;
      }
      &__output--github {
        background: url('~assets/images/github.jpg');
        width: 120px;
        height: 120px;
        animation-delay: 0.6s;
        @include output_logo;
      }
      &__output--twitter {
        background: url('~assets/images/twitter.png');
        width: 120px;
        height: 120px;
        animation-delay: 0.7s;
        @include output_logo;
      }
      &__output--lapras {
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

.switch {
  display: none;
  font-size: 2rem;
  font-weight: 700;
  width: 90%;
  height: 70px;
  line-height: 70px;
  margin-bottom: 20px;
  border-radius: 1rem;
  background-color: burlywood;
  color: saddlebrown;
  text-shadow: 0 2px 0 rgba(255, 255, 255, 0.3), 0 -2px 0 rgba(0, 0, 0, 0.7);
  font-family: font;
}
</style>

<script>
export default {
  data() {
    return {
      description:
        'フロントエンド、PHPを主軸にWeb開発技術を学んでいます。+ 絵描き',
      imageSrc: require('@/assets/images/aocattleya.png'),
      rubberBand: false,
      jello: true,
      bomCount: null,
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
      this.$parent.isActive = true
    },
    collapse() {
      this.bomCount += 1
      if (this.bomCount === 5) {
        this.imageSrc = require('~/assets/images/aocattleyaSorrow.jpg')
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
          300
        )
        setTimeout(
          function() {
            this.bom2 = true
          }.bind(this),
          2000
        )
        setTimeout(
          function() {
            this.bom3 = true
          }.bind(this),
          5500
        )
        setTimeout(
          function() {
            this.bom4 = true
          }.bind(this),
          1800
        )
        setTimeout(
          function() {
            this.bom5 = true
          }.bind(this),
          2300
        )
        setTimeout(
          function() {
            this.bom6 = true
          }.bind(this),
          2800
        )
        setTimeout(
          function() {
            this.bom7 = true
          }.bind(this),
          1500
        )
        setTimeout(
          function() {
            this.bom8 = true
          }.bind(this),
          2500
        )
        this.$emit('bom-event', this.bomCount)
      }
    }
  }
}
</script>
