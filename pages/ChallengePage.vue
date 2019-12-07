<template>
  <div class="container">
    <div class="challenge-data">
      <img class="challenge-image" src="~/assets/design.png" alt="design" />
      <div class="actions">
        <button class="btn">Download Files</button>
        <button class="btn btn-secondary">Tutorial</button>
      </div>
    </div>
    <div class="challenge-info">
      <CodeSnippet
        :challengeName="challengeName"
        :difficulty="difficulty"
        :concepts="concepts"
      />
      <p class="challenge-description">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore, ab
        optio tempore dignissimos minus voluptatem vel harum temporibus saepe
        mollitia voluptatibus aut fugit aliquam itaque, labore eaque soluta.
        Quos molestias odit magnam sit, minima consequatur provident voluptates,
        fugit modi a fugiat culpa corrupti nostrum dolor saepe recusandae
        dolores iste debitis?
      </p>
    </div>
  </div>
</template>

<script>
import CodeSnippet from "~/components/CodeSnippet.vue";

export default {
  name: "ChallengePage",
  components: {
    CodeSnippet
  },
  data() {
    return {
      challengeName: " TabsChallenge",
      difficulty: "junior",
      concepts: ["event listeners", "event bubbling"]
    };
  }
};
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

.actions {
  margin-top: 2.5rem;
  text-align: left;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
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

.challenge-description {
  margin-top: 2.5rem;
  text-align: left;
  line-height: 2;
  color: white;
}

.challenge-image {
  height: 300px;
  max-width: 100%;
}

.links {
  padding-top: 15px;
}
</style>
