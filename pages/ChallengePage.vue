<template>
     <div class="container">
    <div>
      <h1 class="title">
        Front End Challenges
      </h1>
      <h2 class="subtitle">
        Improve your skillz
      </h2>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >
          GitHub
        </a>
        <CodeSnippet
            :challengeName="challengeName"
            :difficulty="difficulty"
            :concepts="concepts"
        />
      </div>
    </div>
  </div>
</template>

<script>
import CodeSnippet from '~/components/CodeSnippet.vue'

export default {
    name: 'ChallengePage',
    components: {
        CodeSnippet
    },
    data () {
        return {
            challengeName: ' TabsChallenge',
            difficulty: 'junior',
            concepts: [
                'event listeners',
                'event bubbling'
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-color: #556271;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: white;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: white;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>