<template>
  <div class="block">
    <p>Reaction Time - {{ score }} ms</p>
    <p class="rank">Rank - {{ rank }}</p>
  </div>
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
    if (this.score < 250) {
      this.rank = "SHEEEEEESH!";
    } else if (this.score < 400) {
      this.rank = "Ight you valid";
    } else {
      this.rank = "Yikes...";
    }
  },
};
</script>

<style>
.block {
  font-size: 1.4rem;
  font-weight: bold;
}
.rank {
  font-size: 1.2rem;
  font-weight: bold;
}
</style>