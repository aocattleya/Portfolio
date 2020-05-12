<template>
  <div>
    <div :class="{ hinge: bom }" class="container animated">
      <div v-show="isActive === false" class="profiles">
        <SignBoard v-on:click.native="toggleSwitch()" v-if="bomCount < 5" />
        <Profile @bom-event="bomLargeFrame" />
      </div>
      <transition appear>
        <div v-show="isActive === true" class="projects-content">
          <Achievement @profile-open="profileOpen" />
        </div>
      </transition>
    </div>
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
  margin: 0 auto;
  background-color: white;
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
      if (bomCount === 5) {
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
