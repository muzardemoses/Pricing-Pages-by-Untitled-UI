<script>
// import UntitledSVG from "../assets/untiltlesd.svg";
// import ExoandSVG from "../assets/expand.svg";
</script>

<template>
  <div
    class="py-5 flex flex-row justify-between items-center px-28 border-b-gray-100 border-b xl:px-10 lg:px-2 md:px-4 md:py-4"
  >
    <div class="flex flex-row justify-between items-center gap-10 ">
      <div>
        <img src="../assets/untiltlesd.svg" alt="logo" />
      </div>
      <div>
        <ul
          class="flex flex-row justify-between items-center gap-9 font-semibold text-base text-gray-600 md:hidden"
        >
          <li>Home</li>
          <li class="flex gap-3 items-center">
            Product
            <span
            class="lg:hidden"
            >
              <img src="../assets/expand.svg" height="10" width="25"   alt="expand" />
            </span>
          </li>
          <li class="flex gap-3 items-center">
            Resources
            <span
            class="lg:hidden"
            >
              <img src="../assets/expand.svg" height="10" width="25"  alt="expand" />
            </span>
          </li>
          <li>Pricing</li>
        </ul>
      </div>
    </div>
    <div class="flex flex-row justify-between items-center gap-3 text-black md:hidden">
      <button class="h-11 w-20 rounded-lg font-semibold text-base text-gray-600">
        Login
      </button>
      <button
        class="btn-col text-white h-11 w-24 rounded-lg border-solid font-semibold text-base bg-violet-600"
      >
        Sign Up
      </button>
    </div>
    <img src="../assets/menu-hamburger.svg" alt="menu" class="hidden md:block" 
      height="25" width="25"
      />
  </div>
</template>

<style scoped>
h1 {
  font-family: "Inter", sans-serif;
}

.btn-col {
  background: #7f56d9;
  /* Primary/600 */

  border: 1px solid #7f56d9;
  /* Shadow/xs */

  box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
}
</style>
