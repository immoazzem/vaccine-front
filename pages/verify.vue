<template>
  <div class="mx-auto">
    <div class="primary-bg text-center">
      <h1 class="text-4xl text-white pb-10 mb-6 font-semibold">
        Vaccine Certificate Verification
      </h1>
    </div>
    <div class="py-20">
      <div class="small-container mx-auto mt-20">
        <div class="bg-white px-20 py-10 border border-gray-100">
          <div class="">
            <h3 class="font-bold text-4xl mb-6 text-center">
              Verify Information
            </h3>

            <div class="">
              <div class="flex -mx-4">
                <div class="w-2/3 px-4">
                  <p class="mb-6">
                    <label for="id_no" class="vacc-label"
                      >National Identity Card Number</label
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
              <p class="mb-6">
                <label for="vc_no" class="vacc-label"
                  >Vaccination Certificate Number</label
                >
                <input
                  id="vc_no"
                  v-model="verifyData.vc_no"
                  type="number"
                  class="vacc-input"
                  placeholder="Type Vaccination Certificate Number"
                />
              </p>

              <p>
                <button @click.prevent="checkInformation" class="primary-btn">
                  Verify Vaccination Certificate
                </button>
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
  name: "",
  components: {},
  data() {
    return {
      verifyData: {
        id_no: "",
        vc_no: "",
        dob: "",
      },
    };
  },
  mounted() {
    this.getAvailableCategories();
    this.getAvailableDivisions();
  },
  methods: {
    getAvailableCategories() {
      this.$axios.get("/categories").then((res) => {
        this.categories = res.data;
      });
    },

    getAvailableDivisions() {
      this.$axios.get("/divisions").then((res) => {
        this.divisions = res.data;
      });
    },

    checkInformation() {
      this.$axios.post("/verify", this.verifyData).then((res) => {
        this.peopleData = res.data;
        if (res.data.success) {
          this.step = "step_2";
        }
      });
    },
  },
};
</script>

<style>
</style>