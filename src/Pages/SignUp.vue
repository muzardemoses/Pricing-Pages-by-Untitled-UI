<template>
    <AuthLayout>
      <template v-slot:auth-contents>
  <form
    @submit.prevent="onSubmit"
    class="pt-24 h-screen flex flex-col items-center w-full">
    <img
      src="../assets/logo.svg"
      alt=""
      height="32"
      width="32"
      class="rounded-lg"
    />
    <h3 class="font-semibold text-3xl text-gray-900 mt-6 mb-3">
      Create an account
    </h3>
    <p class="text-base font-normal text-gray-600">
      Start your 30-day free trial.
    </p>
    <div class="flex flex-col gap-5 mt-8">
      <label for="name" class="flex flex-col gap-1.5">
        <p class="text-sm font-medium text-gray-700">Name*</p>
        <Input
          id="name"
          type="text"
          placeholder="Enter your name"
          v-model="name"
        />
      </label>

      <label for="email" class="flex flex-col gap-1.5">
        <p class="text-sm font-medium text-gray-700">Email*</p>
        <Input
          id="email"
          type="email"
          placeholder="Enter your email"
          v-model="email"
        />
      </label>

      <label for="password" class="flex flex-col gap-1.5">
        <p class="text-sm font-medium text-gray-700">Password*</p>
        <Input
          id="password"
          type="password"
          placeholder="Enter your password"
          v-model="password"
          required
        />
        <p class="text-sm font-normal text-gray-600">
          Must be at least 8 characters.
        </p>
      </label>
    </div>
    <div class="flex flex-col gap-4 mt-6">
      <PurpleButtonVue class="h-11 w360" type="submit" 
        @click="submit"
      >
        Get started
      </PurpleButtonVue>
      <WhiteButtonVue class="h-11 w360 flex items-center justify-center gap-3">
        <img
          src="../assets/google.svg"
          alt="google-icon"
          height="24"
          width="24"
        />
        Sign up with Google
      </WhiteButtonVue>
    </div>
    <div>
        <p class="text-sm font-normal text-gray-600 mt-8">
            Already have an account?
            <RouterLink to="/login" class="text-purple-700 font-semibold">Log in</RouterLink>
        </p>
    </div>
    </form>
</template>
  </AuthLayout>
</template>

<script>
import Input from "../components/Input.vue";
import PurpleButtonVue from "../components/PurpleButton.vue";
import WhiteButtonVue from "../components/WhiteButton.vue";
import { ref } from "vue";
import AuthLayout from "../Layouts/AuthLayout.vue";


export default {
  name: "SectionOne",
  components: {
    Input,
    PurpleButtonVue,
    WhiteButtonVue,
    AuthLayout,
  },
    setup() {
        const name = ref("");
        const email = ref("");
        const password = ref("");
    
        const onSubmit = () => {
        console.log(name.value, email.value, password.value);
        };
    
        return {
        name,
        email,
        password,
        onSubmit,
        };
    },
};
</script>

<style scoped>
form {
  font-family: "Inter", sans-serif;
}

.w360 {
  width: 360px;
}
</style>
