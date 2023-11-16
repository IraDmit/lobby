<template>
  <div class="games">
    <app-LeftPanel />
    <div class="right-col">
      <the-header class="header" />

      <app-games />
    </div>
  </div>
</template>

<script>
import AppGames from "./components/app-games.vue";
import AppLeftPanel from "./components/app-leftPanel.vue";
import theHeader from "./components/navigation/the-header.vue";

export default {
  components: { AppLeftPanel, theHeader, AppGames },
};
</script>

<style lang="scss" scoped>
.games {
  display: grid;
  grid-template-columns: 330px 1fr;
  .header {
    // grid-column: 1 / span 2;
  }
  @media (max-width: 1024px) {
    grid-template-columns: 260px 1fr;
  }
  @media (max-width: 900px) {
    grid-template-columns: 1fr;
  }
}
</style>
