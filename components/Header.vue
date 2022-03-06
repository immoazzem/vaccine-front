<template>
  <div class="primary-bg">
    <div class="container mx-auto py-14">
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
              <li><nuxt-link class="menu-item" to="/registration">Registration</nuxt-link></li>
              <li><nuxt-link class="menu-item" to="/vaccine-card">Card</nuxt-link></li>
              <li><nuxt-link class="menu-item" to="/certificate">Certificate</nuxt-link></li>
              <li><nuxt-link class="menu-item" to="/verify">Verify Certificate</nuxt-link></li>
              <li><nuxt-link class="menu-item" to="/faqs">FAQs</nuxt-link></li>
              <!-- <li><nuxt-link class="menu-item" to="/vcard">VC</nuxt-link></li> -->
            </ul>
          </div>
          <div class="min-w-max">
            <div class="px-6 py-1">
              <nuxt-link class="primary-btn text-base font-medium" to="/registration">Register Now</nuxt-link>
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