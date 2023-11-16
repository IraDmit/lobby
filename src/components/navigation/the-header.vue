<template>
  <header>
    <div class="logo-wrp">
      <img src="@/assets/img/logo_h.png" alt="logo_h" class="logo" />
      <div class="title">Banter</div>
      <div class="part">win</div>
    </div>
    <div class="main">
      <div class="online-wrp">
        <img src="../../assets/img/layers.png" alt="online" />
        <span><span class="count">3578</span>Сейчас в сети</span>
      </div>
      <div class="account">
        <div class="btn btn-blue">
          <!-- <svg class="w-4 h-4" hidden>
            <use xlink:href="@/assets/icons.svg#icon-lock"></use>
          </svg> -->
          Войти
        </div>
        <div class="btn">Регистрация</div>
      </div>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
header {
  background-color: #232832;
  display: flex;
  align-items: center;
  .logo-wrp {
    display: none;
    padding: 20px 60px;

    max-width: 330px;
    width: 100%;
    background-color: #262c38;
    align-items: center;
    justify-content: space-between;
    .logo {
      width: 27px;
      height: 44px;
    }
    .title {
      font-family: Gilroy;
      font-size: 30px;
      line-height: 60px;
      font-weight: 700;
      color: #ffffff;
      @media (max-width: 400px) {
        font-size: 24px;
      }
    }
    .part {
      width: 50px;
      height: 26px;
      background-image: linear-gradient(50deg, #3287fc 12%, #2265c5 87%);
      border-radius: 13.100000000000001px;
      font-family: Gilroy;
      font-size: 16px;
      line-height: 1.2;
      font-weight: 700;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      @media (max-width: 645px) {
        display: none;
      }
    }
    @media (max-width: 1024px) {
      max-width: 260px;
      padding: 20px 30px;
    }
    @media (max-width: 900px) {
      display: flex;
      background-color: unset;
    }
    @media (max-width: 645px) {
      justify-content: unset;
      .logo {
        margin-right: 10px;
      }
    }
    @media (max-width: 470px) {
      padding-right: 0;
    }
  }
  .main {
    padding: 40px 45px;
    padding-bottom: 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    .online-wrp {
      display: flex;
      gap: 7px;
      img {
        width: 17px;
      }
      span {
        font-family: Gilroy;
        font-size: 15px;
        line-height: 1.2;
        font-weight: 700;
        color: #617396;
        .count {
          color: #ffffff;
          margin-right: 7px;
        }
      }
      @media (max-width: 780px) {
        display: none;
      }
    }
    .account {
      display: flex;
      gap: 10px;
      @media (max-width: 470px) {
        gap: 4px;
      }
    }
    @media (max-width: 900px) {
      padding: 10px 45px;
    }
    @media (max-width: 780px) {
      width: auto;
    }
    @media (max-width: 595px) {
      padding: 10px 20px;
    }
    // @media (max-width: 400px) {
    //   padding: 10px 5px;
    // }
  }
  @media (max-width: 780px) {
    justify-content: space-between;
  }
}
</style>
