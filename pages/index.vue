<template>
  <div>
    <div id="loading" v-show="loading">
      <img src="~/assets/images/loading.gif" alt="loading" />
    </div>
    <div id="contents" v-show="!loading">
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
    </div>
  </div>
</template>

<style lang="scss">
@import '~assets/style/_mixins.scss';

#loading {
  width: 100%;
  height: 100vh;
  background-color: #fff;
  position: relative;
}

#loading img {
  position: absolute;
  width: 250px;
  height: 250px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border: dashed 4px #283c5f;
  border-radius: 50%;
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
      loading: true,
      bomCount: null,
      bom: false,
      signboardMsg: '作った物&実績',
      isActive: false
    }
  },
  mounted() {
    setTimeout(() => {
      this.loading = false
    }, 2000)
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
