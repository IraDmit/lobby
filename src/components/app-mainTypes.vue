<template>
  <div>
    <ul class="category-list">
      <li
        v-for="(type, idx) in categoryList"
        :key="`type+${idx}`"
        :style="type.bg"
        class="category"
      >
        <span>{{ type.text }}</span>
        <img :src="getPATH(type.icon)" alt="icon" />
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      categoryList: [
        {
          icon: "corona",
          text: "Slots",
          bg: "background-image: linear-gradient(0.0deg, #ffb81f 0%, #ff731f 100%);",
        },
        {
          icon: "bomb",
          text: "Mines",
          bg: "background-image: linear-gradient(0.0deg, #ff6720 0%, #ff4520 100%);",
        },
        {
          icon: "bubl",
          text: "Bubbles",
          bg: "background-image: linear-gradient(0.0deg, #3d8fff 0%, #4f3dff 100%);",
        },
        {
          icon: "cube",
          text: "Dice ",
          bg: "background-image: linear-gradient(0.0deg, #ff3136 0%, #ff6a24 100%);",
        },
        {
          icon: "roket",
          text: "Crash",
          bg: "background-image: linear-gradient(0.0deg, #c04bff 0%, #ff4ee1 100%); ",
        },
        {
          icon: "coin",
          text: "Coinflip",
          bg: "background-image: linear-gradient(0.0deg, #ffbb42 0%, #ff6643 100%);",
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

<style lang="scss" scoped>
img {
  width: 100%;
}
.category-list {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  gap: 14px;
  margin-top: 60px;
  .category {
    display: flex;
    flex-direction: column;
    padding: 26px;
    border-radius: 20px;
    font-family: Gilroy;
    font-size: 30px;
    line-height: 1.2;
    font-weight: 700;
    color: #ffffff;
    cursor: pointer;
    img {
      margin: 30px 0 50px 0;
      min-height: 119px;
      max-height: 157px;
      object-fit: contain;
      @media (max-width: 768px) {
        margin-bottom: 30px;
        margin-top: 20px;
      }
      @media (max-width: 640px) {
        min-height: 54px;
        max-height: 70px;
      }
      @media (max-width: 450px) {
        margin: 10px 0;
      }
    }
    @media (max-width: 1440px) {
      width: 25%;
      &:nth-child(n + 5) {
        display: none;
      }
    }
    @media (max-width: 950px) {
      padding: 16px;
    }
    @media (max-width: 768px) {
      span {
        font-size: 23px;
      }
    }
    @media (max-width: 595px) {
      width: 33%;
      &:nth-child(n + 4) {
        display: none;
      }
    }
    @media (max-width: 450px) {
      span {
        font-size: 20.9px;
      }
    }
    @media (max-width: 400px) {
      font-size: 18px;
      flex-direction: column;
      justify-content: space-between;
      &:nth-child(3) {
        align-items: center;

        img {
          width: 46px;
          height: 54px;
        }
      }
    }
  }
  @media (max-width: 1440px) {
    display: flex;
    justify-content: space-evenly;
  }
  @media (max-width: 500px) {
    margin-top: 30px;
  }
}
</style>
