<template>
  <a
    v-bind:href="url"
    v-bind:style="delay"
    class="projects__project animated fadeInLeft"
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
      default: '@/assets/images/kurin-github.png'
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
    },
    delay: {
      type: String,
      default: 'animation-delay: 0s;'
    }
  }
}
</script>
