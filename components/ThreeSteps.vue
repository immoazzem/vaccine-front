<template>
  <div>
    <div class="relative py-10">
      <div class="dots-4 right-60 top-0 absolute"></div>
      <div class="container mx-auto">
        <div class="box text-left mb-14">
          <h1 class="text-7xl font-semibold mb-4">3 Steps</h1>
          <p class="text-4xl font-normal">Of Receiving The Covid-19 Vaccine</p>
        </div>
        <div class="box">
          <div class="dots-5 right-10 top-40 absolute"></div>
          <div class="flex text-lg mb-20">
            <div class="w-1/3 pr-16">
              <div class="h-32 flex items-center mb-8">
                <img src="~/static/img/steps-1.svg" alt="" />
              </div>
              <h3 class="font-bold text-2xl mb-6">Online Registration</h3>
              <p>
                First, you have to complete the online registration by verifying
                your national identity card and correct mobile number through
                this portal.
              </p>
            </div>

            <div class="w-1/3 px-8">
              <div class="h-32 flex items-center mb-8">
                <img src="~/static/img/steps-2.svg" alt="" />
              </div>
              <h3 class="font-bold text-2xl mb-6">SMS Notification</h3>
              <p>
                After registering online, you will receive a text message on
                your mobile phone mentioning the date of vaccination and the
                name of the vaccination center.
              </p>
            </div>

            <div class="w-1/3 pl-16">
              <div class="h-32 flex items-center mb-8">
                <img src="~/static/img/steps-3.svg" alt="" />
              </div>
              <h3 class="font-bold text-2xl mb-6">Vaccination</h3>
              <p>
                Subject to receiving a text message on the mobile phone, you
                have to appear in person at the vaccination center on the
                specified date with the vaccine card, national identity card and
                signed consent form to receive the Covid-19 vaccine.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: "ThreeSteps",
};
</script>

<style>
</style>