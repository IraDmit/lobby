<template>
  <div class="games-list">
    <div class="upPanel">
      <span class="title">Новинки</span>
      <span class="all">Все игры</span>
    </div>
    <ul class="games-wrp">
      <li
        class="game"
        v-for="(game, idx) in gamesList"
        :key="`game${idx}`"
        :style="`background-image: url(${getPATH(game.img)})`"
      >
        <span class="name">{{ game.title }}</span>
        <span class="desc">{{ game.desc }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      gamesList: [
        {
          img: "endorphina_Minotaur",
          title: "Gods of the Earth",
          desc: "Pragmatic Play",
        },
        {
          img: "endorphina_Minotaur",
          title: "Gods of the Earth",
          desc: "Pragmatic Play",
        },
        {
          img: "endorphina_Minotaur",
          title: "Gods of the Earth",
          desc: "Pragmatic Play",
        },
        {
          img: "endorphina_Minotaur",
          title: "Gods of the Earth",
          desc: "Pragmatic Play",
        },
        {
          img: "endorphina_Minotaur",
          title: "Gods of the Earth",
          desc: "Pragmatic Play",
        },
        {
          img: "endorphina_Minotaur",
          title: "Gods of the Earth",
          desc: "Pragmatic Play",
        },
      ],
    };
  },
  methods: {
    getPATH(path) {
      return new URL(`../assets/img/${path}.png`, import.meta.url);
    },
  },
};
</script>

<style lang="scss" scoped></style>
