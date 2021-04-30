<template>
  <p>Reaction time: {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    this.rank =
      this.score < 250
        ? "Fast like a Ninja"
        : this.score < 400
        ? "Rapid Reflexes"
        : "Snail pace...";

    // if (this.score < 250) {
    //     this.rank = 'Fast like a Ninja'
    // } else if (this.score < 400) {
    //     this.rank = 'Rapid Reflexes'
    // } else {
    //     this.rank = 'Snail pace...'
    // }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>