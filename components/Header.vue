<template>
  <div class="primary-bg">
    <div class="container mx-auto pt-20 pb-10">
      <div class="bg-white">
        <div class="flex items-center">
          <div class="min-w-max">
            <h2 class="text-2xl text-black font-bold uppercase px-10">
             <nuxt-link to="/">Vaccine</nuxt-link> 
            </h2>
          </div>
          <div class="w-full">
            <ul class="flex justify-center">
              <li><nuxt-link class="menu-item" to="/">Home</nuxt-link></li>
              <li>
                <nuxt-link class="menu-item" to="/registration">Registration</nuxt-link>
              </li>
              <li><nuxt-link class="menu-item" to="/verify">Verify</nuxt-link></li>
              <li><nuxt-link class="menu-item" to="vaccine-card">Vaccine Card</nuxt-link></li>
              <li><nuxt-link class="menu-item" to="/help">HelpGuide</nuxt-link></li>
              <li><nuxt-link class="menu-item" to="/faqs">FAQs</nuxt-link></li>
            </ul>
          </div>
          <div class="min-w-max">
            <div class="px-6">
              <nuxt-link class="primary-btn" to="/registration">Register Now</nuxt-link>
            </div>
          </div>
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