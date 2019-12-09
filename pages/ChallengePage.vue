<template>
  <div class="container">
    <div class="challenge-container">
      <div class="challenge-data">
        <transition name="slideout">
          <div v-if="shown">
            <img class="challenge-image" src="~/assets/design.png" alt="design" />
            <div class="actions">
              <button class="btn">Download Files</button>
              <button class="btn btn-secondary">Tutorial</button>
            </div>
          </div>
        </transition>
      </div>
      <div class="challenge-info">
        <transition name="slideout-right">
          <div v-if="secondShown">
            <CodeSnippet
              :challengeName="challengeName"
              :difficulty="difficulty"
              :concepts="concepts"
            />
            <p class="challenge-description">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore, ab
              optio tempore dignissimos minus voluptatem vel harum temporibus saepe
              mollitia voluptatibus aut fugit aliquam itaque, labore eaque soluta.
              Quos molestias odit magnam sit, minima consequatur provident
              voluptates, fugit modi a fugiat culpa corrupti nostrum dolor saepe
              recusandae dolores iste debitis?
            </p>
          </div>
        </transition>
      </div>
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
      concepts: ["event listeners", "event bubbling"],
      shown: false,
      secondShown: false
    };
  },
  mounted() {
    this.secondShown = true;
    setTimeout(() => {
      this.shown = true;
    }, 500);
  }
};
</script>

<style lang="scss" scoped>
.container {
  // add mobile stle with breakpoint
  margin: 0 auto;
  min-height: 100vh;
  max-width: 1200px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  text-align: center;
}

.challenge-container {
  display: flex;
  justify-content: space-around;
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

.slideout-enter {
  transform: translateX(-600px);
  opacity: 0;
}

.slideout-right-enter {
  transform: translateX(600px);
  opacity: 0;
}

.slideout-enter-active,
.slideout-right-enter-active {
  transition: transform 0.6s, opacity 0.8s;
}
// .slide-left-children-enter, .slide-left-children-leave-to {
//   transform: translateX(-250px);
//   opacity: 0;
// }

// .slide-left-children-enter-active, .slide-left-children-leave-active {
//   transition: transform 0.6s, opacity 1s;
// }
</style>
