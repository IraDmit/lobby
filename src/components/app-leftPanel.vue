<template>
  <aside :class="{ show: isMenuOpen }">
    <div class="logo-wrp">
      <img src="@/assets/img/logo_h.png" alt="logo_h" class="logo" />
      <div class="title">Banter</div>
      <div class="part">win</div>
    </div>
    <ul class="main-pages">
      <li class="page">
        <a href="#" class="main">
          <div class="image">
            <img src="@/assets/img/main_page.png" alt="icon" />
          </div>
          <span>Главная</span>
        </a>
      </li>
      <li class="page">
        <a href="#" class="active">
          <img src="@/assets/img/slots.png" alt="icon" />
          <span>Slots</span>
        </a>
      </li>
      <li class="page">
        <a href="#">
          <img src="@/assets/img/mines.png" alt="icon" />
          <span>Mines</span>
        </a>
      </li>
      <li class="page">
        <a href="#">
          <img src="@/assets/img/bubbles.png" alt="icon" />
          <span>Bubbles</span>
        </a>
      </li>
      <li class="page">
        <a href="#">
          <img src="@/assets/img/dice.png" alt="icon" />
          <span>Dice</span>
        </a>
      </li>
    </ul>
    <ul class="support_pages">
      <li class="page">
        <a href="#">
          <img src="@/assets/img/faq.png" alt="icon" /> <span>FAQ</span>
        </a>
      </li>
      <li class="page">
        <a href="#">
          <img src="@/assets/img/bonus.png" alt="icon" /> <span>Бонусы</span>
        </a>
      </li>
      <li class="page">
        <a href="#">
          <img src="@/assets/img/referals.png" alt="icon" />
          <span>Реферальная</span>
        </a>
      </li>
      <li class="page">
        <a href="#">
          <img src="@/assets/img/turnirs.png" alt="icon" /> <span>Турниры</span>
        </a>
      </li>
      <li class="page">
        <a href="#">
          <img src="@/assets/img/support.png" alt="icon" />
          <span>Поддержка</span>
        </a>
      </li>
      <li class="page">
        <a href="#">
          <img src="@/assets/img/settings.png" alt="icon" />
          <span>Настройки</span>
        </a>
      </li>
    </ul>

    <div class="down-panel">
      <!-- <div
        :class="!state ? 'h-[92px] w-[46px]' : 'w-[92px] h-[46px]'"
        hidden
        class="relative flex flex-wrap items-stretch rounded-full bg-[#2b323f] dark:bg-[#e4ecff]"
      >
        <button
          @click="setLightTheme"
          :class="{ active: light }"
          class="focus:outline-none w-[46px] relative z-[1] flex items-center rounded-full justify-center transition-all duration-200 ease-linear text-[#617396] hover:text-[#8ea3ce] dark:hover:[&:not(.active)]:text-[#4f5d7a] [&.active]:text-white"
          type="button"
        >
          <svg class="w-5 h-5">
            <use xlink:href="@/assets/icons.svg#icon-light"></use>
          </svg>
        </button>
        <button
          @click="setDarkTheme"
          :class="{ active: !light }"
          class="focus:outline-none w-[46px] relative z-[1] flex items-center rounded-full justify-center transition-all duration-200 ease-linear text-[#617396] hover:text-[#8ea3ce] dark:hover:[&:not(.active)]:text-[#4f5d7a] [&.active]:text-white"
          type="button"
        >
          <svg class="w-5 h-5">
            <use xlink:href="@/assets/icons.svg#icon-night"></use>
          </svg>
        </button>
        <span
          :class="[
            light ? 'bg-[#3a81e3]' : 'bg-[#434c5e]',
            !state ? 'h-[46px] w-full' : 'w-[46px] h-full',
            !light && state ? 'translate-x-full' : '',
            !light && !state ? 'translate-y-full' : '',
          ]"
          class="absolute left-0 top-0 rounded-full transition-all duration-[100ms] ease-linear"
        ></span>
      </div> -->
    </div>
  </aside>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
    };
  },
};
</script>

<style lang="scss" scoped>
aside {
  background-color: #262c38;
  max-width: 330px;
  width: 100%;
  font-family: Gilroy;
  font-size: 17px;
  line-height: 1.2;
  font-weight: 700;
  color: #617396;
  height: 100%;
  padding: 20px 60px;
  padding-left: 40px;
  .logo-wrp {
    padding: 20px 15px;
    display: flex;
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
      padding: 20px;
    }
    @media (max-width: 900px) {
      display: none;
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
  ul {
    list-style: none;
    display: flex;
    flex-direction: column;

    margin: 0;
    padding: 0;
  }
  .main-pages {
    margin-bottom: 60px;
    position: relative;
    &::after {
      content: "";
      position: absolute;
      bottom: -30px;
      left: 20px;
      width: 107px;
      height: 3px;
      border-radius: 1.5px;
      background-color: #2c3340;
    }
  }
  .page {
    font-size: 17px;
    line-height: 1.2;
    font-weight: 700;
    cursor: pointer;
    transition: 0.3s;

    a {
      padding: 16px 20px;
      text-decoration: none;
      display: flex;
      gap: 20px;
      color: #617396;
      align-items: center;
      &.active {
        background-color: #2b323f;
        border-radius: 30px;
        span {
          color: #fff;
        }
      }
    }
    &:hover {
      span {
        color: #fff;
        z-index: 1;
      }
    }
    span {
      z-index: 1;
    }
    img {
      width: 23px;
      z-index: 1;
      height: 23px;
      object-fit: cover;
      pointer-events: none;
    }
    .main {
      padding-left: 12px;
      .image {
        display: flex;
        padding: 8px;
        background-image: linear-gradient(50deg, #3287fc 2%, #2265c5 97%);
        border-radius: 14px;
        img {
          width: 17px;
          height: 17px;
        }
      }
    }
  }
  @media (max-width: 1024px) {
    padding: 20px 30px;
  }
  @media (max-width: 900px) {
    display: none;
    position: fixed;
    height: fit-content;
    right: 20px;
    bottom: 30px;
    border-radius: 30px;
    max-width: 240px;
    .main-pages {
      display: none;
    }
  }
}
.show {
  @media (max-width: 900px) {
    display: block;
  }
}
</style>
