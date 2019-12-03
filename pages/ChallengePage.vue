<template>
    <div class="container">
    <div class="challenge-data">
        <img src="" alt="">
        <div class="actions">
            <button>Download Files</button>
            <button>Tutorial</button>
        </div>
    </div>
    <div class="challenge-info">
        <CodeSnippet
            :challengeName="challengeName"
            :difficulty="difficulty"
            :concepts="concepts"
        />
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
  margin: 8rem auto;
  min-height: 100vh;
  max-width: 1200px;
  display: flex;
  justify-content: space-around;
  align-items: flex-start;
  text-align: center;
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

.challenge-info {
    width: 50%;
}

.challenge-data {
    width: 40%;
}

.links {
  padding-top: 15px;
}
</style>