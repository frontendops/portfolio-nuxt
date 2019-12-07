<template>
  <ChallengePage />
</template>

<script>
import ChallengePage from "@/pages/ChallengePage";

export default {
  components: {
    ChallengePage
  }
};
</script>

<style lang="scss">
body {
  background-color: #556271;
}

.btn {
  background: none;
  padding: 0.5rem 0.75rem;
  color: white;
  font-weight: bold;
  font-size: 1rem;
  border-radius: 10px;
  border: 1px solid whitesmoke;
}

.btn-secondary {
  background: whitesmoke;
  color: #556271;
}
</style>
