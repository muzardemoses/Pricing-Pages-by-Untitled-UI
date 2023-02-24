<template>
  <div
    class="py-5 flex flex-row justify-between items-center px-28 border-b-gray-100 border-b xl:px-10 lg:px-2 md:px-4 md:py-4"
  >
    <div class="flex flex-row justify-between items-center gap-10">
      <div>
        <img src="../assets/untiltlesd.svg" alt="logo" />
      </div>
      <div>
        <ul
          class="flex flex-row justify-between items-center gap-9 font-semibold text-base text-gray-600 md:hidden"
        >
          <li>
            <a href=""> Home </a>
          </li>
          <li>
            <a href="" class="flex gap-3 items-center">
              Product
              <span class="lg:hidden">
                <img
                  src="../assets/expand.svg"
                  height="10"
                  width="25"
                  alt="expand"
                />
              </span>
            </a>
          </li>
          <li>
            <a href="" class="flex gap-3 items-center">
              Resources
              <span class="lg:hidden">
                <img
                  src="../assets/expand.svg"
                  height="10"
                  width="25"
                  alt="expand"
                />
              </span>
            </a>
          </li>
          <li>
            <a href="">
            Pricing
            </a>
          </li>
        </ul>
      </div>
    </div>
    <div
      class="flex flex-row justify-between items-center gap-3 text-black md:hidden"
    >
      <button
        class="h-11 w-20 rounded-lg font-semibold text-base text-gray-600"
      >
        Login
      </button>
      <PurpleButton class="h-11 w-24 r"> Sign Up </PurpleButton>
    </div>
    <img
      src="../assets/menu-hamburger.svg"
      alt="menu"
      class="hidden md:block"
      height="25"
      width="25"
    />
  </div>
</template>

<style scoped>
h1 {
  font-family: "Inter", sans-serif;
}
</style>

<script>
import PurpleButton from "./PurpleButton.vue";
import WhiteButton from "./WhiteButton.vue";

export default {
  name: "Header",
  components: {
    PurpleButton,
    WhiteButton,
  },
};
</script>
