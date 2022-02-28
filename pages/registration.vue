<template>
  <div>
    <div class="mx-auto mt-20 pb-10">
      <div class="container mx-auto text-center">
        <h3 class="text-6xl font-bold mb-10">Vaccine Registration</h3>
        <p class="leading-7 text-lg font-normal">
          Complete the registration by verifying your national identity card and
          mobile number in the form below. The place and date of delivery of the
          vaccine will be informed in due course through SMS message on the
          mobile phone.
        </p>
      </div>
    </div>
    <div class="py-20">
      <div class="relative">
        <div class="container mx-auto small-container text-center pt-20">
          <div>
            <div class="text-center">
              <h2 class="text-4xl text-black mb-6 font-semibold">
                Register for Vaccine
              </h2>
              <p class="text-lg">
                You will just need your NID Card, Phone number and filling up
                some info
              </p>
            </div>
          </div>
        </div>
      </div>
      <div class="mx-auto small-container text-center">
        <div class="">
          <div class="max-w-screen-sm mx-auto">
            <VaccineSteps theme="step_1" />
          </div>
        </div>
      </div>
      <div class="relative py-10">
        <div class="dots-1 left-20 top-0 absolute"></div>
        <div class="down-arrow left-1/2 absolute"></div>
      </div>
      <div class="small-container mx-auto mt-20">
        <div class="bg-white px-20 py-10 border border-gray-100">
          <div class="">
            <h3 class="font-bold text-4xl mb-6 text-center">
              Identity Verification
            </h3>

            <div v-if="peopleData.hasOwnProperty('success') && !peopleData.success" class="bg-red-200 text-red-900 p-4 mb-6">
                {{ peopleData.message }}
              </div>

            <p class="mb-6">
              <label class="vacc-label" for="category_id"
                >Select Category
              </label>
              <select
                name=""
                v-model="verifyData.category_id"
                id="category_id"
                class="vacc-input"
              >
                <option selected="selected" value="">Select a category</option>
                <option
                  v-for="item in categories"
                  :key="item.id"
                  :value="item.id"
                >
                  {{ item.name }}
                </option>
              </select>
            </p>

            <div v-if="verifyData.category_id" class="flex -mx-4">
              <div class="w-2/3 px-4">
                <p class="mb-6">
                  <label for="id_no" class="vacc-label"
                    >National ID Number</label
                  >
                  <input
                    id="id_no"
                    v-model="verifyData.id_no"
                    type="number"
                    class="vacc-input"
                    placeholder="Type your national ID card number"
                  />
                </p>
              </div>
              <div class="w-1/3 px-4">
                <p class="mb-6">
                  <label for="dob" class="vacc-label">Date of birth</label>
                  <input
                    id="dob"
                    v-model="verifyData.dob"
                    type="date"
                    class="vacc-input"
                    placeholder="Type your national ID card number"
                  />
                </p>
              </div>
            </div>
            <p>
              <button @click.prevent="checkInformation" class="primary-btn">
                Check my information
              </button>
            </p>
          </div>

          <div></div>

          <div></div>
        </div>
      </div>
      <div class="threesteps mt-24">
        <ThreeSteps />
      </div>
    </div>
  </div>
</template>

<script>
import VaccineSteps from "../components/VaccineSteps";
import ThreeSteps from "../components/ThreeSteps";
export default {
  name: "registration",
  components: {
    VaccineSteps,
    ThreeSteps,
  },
  data() {
    return {
      categories: [],
      peopleData: [],
      verifyData: {
        category_id: "",
        id_no: "",
        dob: "",
      },
    };
  },
  mounted() {
    this.getAvailableCategories();
    // this.checkInformation();
  },
  methods: {
    getAvailableCategories() {
      this.$axios.get("/categories").then((res) => {
        this.categories = res.data;
      });
    },

    checkInformation() {
      this.$axios.post("/verify", this.verifyData).then((res) => {
        this.peopleData = res.data;
      });
    },
  },
};
</script>

<style>
</style>