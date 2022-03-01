<template>
  <div>
    <div class="flex -mx-6 my-16">
      <div class="flex-1 px-6">
        <div class="h-32 flex justify-center items-center">
          <img class="mx-auto" src="~/static/img/nid.svg" alt="" />
        </div>
        <div
          class="
            border-4
            w-6
            h-6
            rounded-full
            border-green-600
            mx-auto
            mb-4
            mt-8
            tika-step
            relative
          "
        ></div>
        <p class="text-lg font-bold">NID</p>
      </div>

      <div class="flex-1 px-6">
        <div class="h-32 flex justify-center items-center">
          <img v-if="theme == 'homepage' || theme == 'step_2' || theme == 'step_3'" class="mx-auto" src="~/static/img/information.svg" alt="" />
          <img v-if="theme == 'step_1'" class="mx-auto" src="~/static/img/information-disabled.svg" alt="" />
        </div>
        <div v-bind:class="theme == 'homepage' || theme == 'step_2 ' || theme == 'step_3' ? 'border-green-600' : 'border-gray-400'" class=" border-4 w-6 h-6 rounded-full mx-auto mb-4 mt-8 tika-step relative"></div>
        <p class="text-lg font-bold">Information</p>
      </div>

      <div class="flex-1 px-6">
        <div class="h-32 flex justify-center items-center">
          <img v-if="theme == 'homepage' || theme == 'step_3'" class="mx-auto" src="~/static/img/phone.svg"  alt="" />
          <img v-if="theme == 'step_1' || theme == 'step_2'" class="mx-auto" src="~/static/img/phone-disabled.svg" alt="" />
        </div>
        <div v-bind:class="theme == 'homepage' || theme == 'step_3' ? 'border-green-600' : 'border-gray-400'" class=" border-4 w-6 h-6 rounded-full mx-auto mb-4 mt-8 tika-step relative"></div>
        <p class="text-lg font-bold">Phone</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "VaccineSteps",
    props: ["theme"],
};
</script>

<style>
</style>