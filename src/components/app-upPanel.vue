<template>
  <div class="upPanel">
    <input
      type="text"
      class="custom-input"
      placeholder="Например: The Dog House"
    />
    <div class="right">
      <div class="filter">
        <img src="@/assets/img/heart.png" alt="icon" />
        <span>Избранное</span>
      </div>
      <div class="filter">
        <img src="@/assets/img/burger.png" alt="icon" />
        <span>Провайдеры</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.upPanel {
  display: flex;
  justify-content: space-between;
  position: relative;
  .custom-input {
    background-color: #262c38;
    border-radius: 23.5px;
    padding: 15px;
    border: none;
    font-family: Gilroy;
    font-size: 17px;
    line-height: 1.2;
    font-weight: 700;
    max-width: 320px;
    width: 100%;
    margin-right: 15px;
    &::placeholder {
      color: #617396;
    }
    @media (max-width: 576px) {
      width: 100%;
      margin-right: 0;
      max-width: unset;
    }
  }
  .right {
    display: flex;
    gap: 45px;
    .filter {
      cursor: pointer;
      display: flex;
      gap: 10px;
      align-items: center;
      font-family: Gilroy;
      font-size: 17px;
      line-height: 1.2;
      font-weight: 700;
      color: #ffffff;
      @media (max-width: 645px) {
        span {
          display: none;
        }
      }
    }
    @media (max-width: 768px) {
      gap: 20px;
    }
    @media (max-width: 576px) {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      right: 20px;
    }
  }
}
</style>
