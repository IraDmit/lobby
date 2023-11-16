<template>
  <div class="mobileMenu absolute right-0">
    <Transition
      enter-active-class="transition-all duration-200 ease"
      enter-class="scale-95 opacity-0"
      enter-to-class="scale-100 opacity-100"
      leave-active-class="transition-all duration-200 ease"
      leave-class="scale-100 opacity-100"
      leave-to-class="scale-95 opacity-0"
    >
      <div
        class="w-[220px] origin-top-right overflow-hidden flex flex-col py-2 bg-[#282f3c] dark:bg-white rounded-[16px] relative z-[1]"
      >
        <ul class="flex flex-col">
          <li
            v-for="(item, index) in profileMenu"
            v-show="!item.mobile"
            :key="index"
          >
            <router-link
              :to="item.url"
              class="flex items-center gap-3 text-[#617396] dark:text-[#1A2D4C] font-[700] py-2 px-4 group transition-all duration-200 ease-linear hover:text-white dark:hover:text-[#398dff] hover:bg-white/[0.02] dark:hover:bg-[#398dff]/[0.1]"
            >
              <svg
                class="w-4 h-4 group-hover:text-[#398dff] group-[.active]:text-[#398dff] transition-all duration-200 ease-linear"
              >
                <use
                  :xlink:href="require('@/assets/icons.svg') + '#' + item.ico"
                ></use>
              </svg>
              {{ item.name }}
            </router-link>
          </li>
          <li
            class="min-[945px]:!hidden"
            v-for="(item, index) in profileMenu"
            v-show="item.mobile"
            :key="index"
          >
            <router-link
              :to="item.url"
              class="flex items-center gap-3 text-[#617396] dark:text-[#1A2D4C] font-[700] py-2 px-4 group transition-all duration-200 ease-linear hover:text-white dark:hover:text-[#398dff] hover:bg-white/[0.02] dark:hover:bg-[#398dff]/[0.1]"
            >
              <svg
                class="w-4 h-4 group-hover:text-[#398dff] group-[.active]:text-[#398dff] transition-all duration-200 ease-linear"
              >
                <use
                  :xlink:href="require('@/assets/icons.svg') + '#' + item.ico"
                ></use>
              </svg>
              {{ item.name }}
            </router-link>
          </li>
          <li @click="exit()">
            <a
              href="javascript:;"
              class="flex items-center gap-3 text-[#617396] dark:text-[#1A2D4C] font-[700] py-2 px-4 group transition-all duration-200 ease-linear hover:text-white dark:hover:text-[#398dff] hover:bg-white/[0.02] dark:hover:bg-[#398dff]/[0.1]"
            >
              <svg
                class="w-4 h-4 group-hover:text-[#398dff] group-[.active]:text-[#398dff] transition-all duration-200 ease-linear"
              >
                <use xlink:href="@/assets/icons.svg#icon-logout"></use>
              </svg>
              Выход
            </a>
          </li>
        </ul>
      </div>
    </Transition>
    <Transition
      enter-active-class="transition-all duration-200 ease"
      enter-class="opacity-0"
      enter-to-class="opacity-100"
      leave-active-class="transition-all duration-200 ease"
      leave-class="opacity-100"
      leave-to-class="opacity-0"
    >
      <div
        @click="dropdown = false"
        class="fixed cursor-pointer left-0 top-0 w-full h-full bg-[#232934]/[0.8] dark:bg-black/[0.8] backdrop-blur-[10px]"
      ></div>
    </Transition>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.mobileMenu {
  bottom: calc(-90vh);
}
</style>
