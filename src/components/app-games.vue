<template>
  <div class="mainInfo">
    <appUpPanel />
    <app-mainTypes />
    <app-popular />
    <app-newGames />
    <div class="btn btn-blue btn-big">Показать все</div>
  </div>
</template>

<script>
import AppMainTypes from "./app-mainTypes.vue";
import AppNewGames from "./app-newGames.vue";
import AppPopular from "./app-popular.vue";
import AppUpPanel from "./app-upPanel.vue";
AppNewGames;
export default {
  components: { AppUpPanel, AppMainTypes, AppPopular, AppNewGames },
};
</script>

<style lang="scss" scoped>
.mainInfo {
  padding: 40px 45px;
  background-color: #232832;
  padding-top: 20px;
  display: flex;
  flex-direction: column;
  .btn {
    display: inline-flex;
    margin: 40px auto 0 auto;
    align-self: center;
  }
  @media (max-width: 645px) {
    padding: 10px 20px;
  }
}
</style>
