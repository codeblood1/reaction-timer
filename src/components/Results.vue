<template>
  <p class="score">Reaction Time: {{ score }} ms</p>
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
    if (this.score < 250) {
      this.rank = "Rugged You!!!";
    } else if (this.score < 400) {
      this.rank = "You Try!!";
    } else {
      this.rank = "Too Slow(your hand de pain you?)";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4rem;
  color: #eee;
  font-weight: bold;
}
.rank:hover {
  font-size: 1.4rem;
  color: aqua;
  font-weight: bold;
}
.score {
  color: aqua;
  font-size: 25px;
}
.score:hover {
  color: #eee;
  font-size: 24px;
}
</style>
