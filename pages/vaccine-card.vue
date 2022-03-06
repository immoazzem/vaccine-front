<template>
  <div>
    <div class="mx-auto">
      <div class="primary-bg text-center">
        <h1 class="text-4xl text-white pb-10 mb-6 font-semibold">
          Vaccine Card Download
        </h1>
      </div>
      <div class="py-20">
        <div class="small-container mx-auto mt-20">
          <div class="bg-white px-20 py-10 border border-gray-100">
            <div v-if="isVerified == false" class="">
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
                <p>
                  <button @click.prevent="checkInformation" class="primary-btn">
                    Verify
                  </button>
                </p>
              </div>
            </div>

            <div v-if="isVerified == true">
              <div v-if="step == 'step_1'">
                <h3 class="font-bold text-4xl mb-6 text-center">
                  NID Verified
                </h3>

              </div>
              <div v-if="step == 'step_2'">
                <h3 class="font-bold text-xl mb-6 text-center">
                  Not Data Found! Reigster First
                </h3>
              </div>
            </div>


          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Vaccine-Card",
  components: {},
  data() {
    return {
      verifyData: {
        category_id: '1',
        id_no: "",
        dob: ""
      },
      isVerified: false,
      step: '',
      peopleData: [],
      
    };
  },
  mounted() {
  },
  methods: {
    checkInformation() {
      this.$axios.post("/verify", this.verifyData).then((res) => {
        this.peopleData = res.data;
        if (res.data.success) {
          this.isVerified = true;
          this.step = "step_1";
        } else if (res.data.success == false) {
          this.isVerified = true;
          this.step = "step_2";
        }
      });
    },

  },
};
</script>

<style>
</style>