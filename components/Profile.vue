<template>
  <div class="profiles__profile animated fadeIn">
    <img
      v-on:click=";(rubberBand = !rubberBand), (jello = !jello), collapse()"
      :class="{ rubberBand: rubberBand, jello: jello, bounceOutUp: bom5 }"
      :src="imageSrc"
      class="profiles__profile__logo animated"
    />
    <img
      :class="{ hinge: bom1 }"
      src="~/assets/images/name.png"
      class="profiles__profile__name animated"
    />
    <h2 :class="{ hinge: bom2 }" class="profiles__profile__subtitle animated">
      {{ description }}
    </h2>
    <div :class="{ hinge: bom3 }" class="profiles__profile__links animated">
      <a
        :class="{ hinge: bom4 }"
        class="profiles__profile__links__output_logo animated flipInX"
        href="https://connpass.com/user/aocattleya/"
        target="_blank"
        rel="noopener noreferrer"
      >
      </a>
      <a
        :class="{ hinge: bom5 }"
        class="profiles__profile__links__output_logo animated flipInX"
        href="https://qiita.com/aocattleya"
        target="_blank"
        rel="noopener noreferrer"
      ></a>
      <a
        :class="{ hinge: bom6 }"
        class="profiles__profile__links__output_logo animated flipInX"
        href="https://github.com/aocattleya"
        target="_blank"
        rel="noopener noreferrer"
      ></a>
      <a
        :class="{ hinge: bom7 }"
        class="profiles__profile__links__output_logo animated flipInX"
        href="https://twitter.com/aocattleya"
        target="_blank"
        rel="noopener noreferrer"
      ></a>
      <a
        :class="{ hinge: bom8 }"
        class="profiles__profile__links__output_logo animated flipInX"
        href="https://lapras.com/public/QIOCQBE"
        target="_blank"
        rel="noopener noreferrer"
      ></a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      description:
        '趣味でフロントエンドを主軸にWeb技術を学んでいます。+ 絵描き🎨',
      imageSrc: require('@/assets/images/aocattleya.jpg'),
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
    collapse() {
      this.bomCount += 1
      if (this.bomCount === 10) {
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
