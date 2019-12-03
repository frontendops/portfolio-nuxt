<template>
 <ChallengePage />
</template>

<script>
import Logo from '~/components/Logo.vue'
import CodeSnippet from '~/components/CodeSnippet.vue'
import ChallengePage from './ChallengePage.vue'

export default {
  components: {
    Logo,
    CodeSnippet,
    ChallengePage
  }
}
</script>

<style lang="scss">
  body {
    background-color: #556271;
  }
</style>
