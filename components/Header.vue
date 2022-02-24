<template>
  <div class="primary-bg">
    <div class="container mx-auto py-20">
      <div class="bg-white mb-20">
        <div class="flex items-center">
          <div class="min-w-max">
            <h2 class="text-2xl text-black font-bold uppercase px-10">
              Vaccine
            </h2>
          </div>
          <div class="w-full">
            <ul class="flex justify-center">
              <li><nuxt-link class="menu-item" to="">Home</nuxt-link></li>
              <li>
                <nuxt-link class="menu-item" to="">Registration</nuxt-link>
              </li>
              <li><nuxt-link class="menu-item" to="">Verify</nuxt-link></li>
              <li><nuxt-link class="menu-item" to="">Download</nuxt-link></li>
              <li><nuxt-link class="menu-item" to="">HelpGuide</nuxt-link></li>
              <li><nuxt-link class="menu-item" to="">FAQs</nuxt-link></li>
            </ul>
          </div>
          <div class="min-w-max">
            <div class="px-6">
              <nuxt-link class="primary-btn" to="">Register Now</nuxt-link>
            </div>
          </div>
        </div>
      </div>

      <div class="flex">
        <div class="w-full">
          <h1
            class="
              hero-heading
              font-bold
              text-white
              uppercase
              leading-none
              mb-8
            "
          >
            Vaccine
          </h1>
          <h2 class="font-medium text-7xl text-white mb-8">Registration</h2>
          <p class="text-2xl text-white leading-9 mb-8">
            Complete the registration by verifying your national identity card
            and mobile number
          </p>
          <div class="pt-2 flex rounded-3xl bg-white relative s-inp-box">
              <input type="text" class="w-full ml-1 -mr-20 -mt-2 rounded-3xl">
              <button class="w-1/6 -mt-1 my-1 primary-bg rounded-3xl -mr-1">Go</button>
          </div>
        </div>
        <div class="min-w-max">
            <img src="~/static/img/hero.png" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  components: {},
};
</script>

<style>
</style>