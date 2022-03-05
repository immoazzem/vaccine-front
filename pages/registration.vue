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
            <VaccineSteps :theme="step" />
          </div>
        </div>
      </div>
      <div class="relative py-10">
        <div class="dots-1 left-20 top-0 absolute"></div>
        <div class="down-arrow left-1/2 absolute"></div>
      </div>
      <div class="small-container mx-auto mt-20">
        <div class="bg-white px-20 py-10 border border-gray-100">
          <div v-if="step == 'step_1'" class="">
            <h3 class="font-bold text-4xl mb-6 text-center">
              Identity Verification
            </h3>

            <div
              v-if="peopleData.hasOwnProperty('success') && !peopleData.success"
              class="bg-red-200 text-red-900 p-4 mb-6"
            >
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

          <div v-if="step == 'step_2'" class="">
            <h3 class="font-bold text-4xl mb-6 text-center">
              Verify All Information
            </h3>
            <p class="mb-6">
              <label class="vacc-label" for="division_id"
                >Select Division</label
              >
              <select
                @change.prevent="getAvailableDistricts"
                name=""
                v-model="division_id"
                id="division_id"
                class="vacc-input"
              >
                <option selected="selected" value="">Select Division</option>
                <option
                  v-for="item in divisions"
                  :key="item.id"
                  :value="item.id"
                >
                  {{ item.name }}
                </option>
              </select>
            </p>

            <p v-if="districts.length" class="mb-6">
              <label class="vacc-label" for="district_id"
                >Select Districts</label
              >
              <select
                @change.prevent="getAvailableUpazilas"
                name=""
                v-model="district_id"
                id="district_id"
                class="vacc-input"
              >
                <option selected="selected" value="">Select District</option>
                <option
                  v-for="item in districts"
                  :key="item.id"
                  :value="item.id"
                >
                  {{ item.name }}
                </option>
              </select>
            </p>

            <p v-if="upazilas.length" class="mb-6">
              <label class="vacc-label" for="upazila_id">Select Upazila</label>
              <select
                @change.prevent="getAvailableCenters"
                name=""
                v-model="upazila_id"
                id="upazila_id"
                class="vacc-input"
              >
                <option selected="selected" value="">Select Upazila</option>
                <option
                  v-for="item in upazilas"
                  :key="item.id"
                  :value="item.id"
                >
                  {{ item.name }}
                </option>
              </select>
            </p>

            <p v-if="centers.length" class="mb-6">
              <label class="vacc-label" for="center_id"
                >Select Vaccination Center
              </label>
              <select v-model="center_id" class="vacc-input" id="center_id">
                <option selected="selected" value="">Select a center</option>
                <option v-for="item in centers" :key="item.id" :value="item.id">
                  {{ item.name }}
                </option>
              </select>
            </p>

            <p v-if="!centers.length && upazila_id">No center available</p>

            <div v-if="center_id" class="">
              <p class="mb-6">
                <label for="name" class="vacc-label">Name</label>
                <input
                  id="name"
                  v-model="name"
                  type="text"
                  class="vacc-input"
                  placeholder="Type your name"
                />
              </p>
              <p class="mb-6">
                <label for="diabates" class="vacc-label"
                  >Do you have diabates?</label
                >
                <select v-model="diabates" class="vacc-input" id="diabates">
                  <option selected="selected" value="">Select a value</option>
                  <option value="1">Yes</option>
                  <option value="0">No</option>
                </select>
              </p>

              <p v-if="diabates">
                <button @click.prevent="goToStepThree" class="primary-btn">
                  Submit
                </button>
              </p>
            </div>
          </div>

          <div v-if="step == 'step_3'">
            <h3 class="font-bold text-4xl mb-6 text-center">
              Phone verification
            </h3>

            <div v-if="!smsSent">
              <p class="mb-6">
                <label for="phone_no" class="vacc-label">Phone number</label>
                <input
                  id="phone_no"
                  v-model="phone_no"
                  type="text"
                  class="vacc-input"
                  placeholder="Type phone number"
                />
              </p>
              <p>
                <button
                  @click.prevent="sendVerificationSMS"
                  class="primary-btn"
                >
                  Send SMS
                </button>
              </p>
            </div>

            <div v-if="smsSent">
              <p class="mb-6">
                <label for="verify_code" class="vacc-label"
                  >Verification code</label
                >
                <input
                  id="verify_code"
                  v-model="verify_code"
                  type="text"
                  class="vacc-input"
                  placeholder="Type verification code"
                />
              </p>
              <p>
                <button
                  @click.prevent="
                    verifyCode();
                    registerPeople();
                  "
                  class="primary-btn"
                >
                  Verify
                </button>
              </p>
            </div>
          </div>

          <div v-if="step == 'step_4'" class="flex-wrap mx-auto text-center">
            <div class="flex flex-col min-w-max mx-auto mb-8">
              <img
                src="~/static/img/checkmark-success.svg"
                alt=""
                class="w-20 h-20 mx-auto"
              />
            </div>
            <div class="w-full mx-auto mb-8">
              <h1 class="text-4xl font-bold text-black">
                Registration Successful
              </h1>
            </div>
            <div class="w-full mx-auto">
              <p>
                <button @click.prevent="getRegStatus" class="primary-btn">
                  See Registration Status
                </button>
              </p>
            </div>
          </div>

          <div v-if="step == 'step_5'" class="">
            <div>
              <!-- This example requires Tailwind CSS v2.0+ -->
              <div class="flex flex-col">
                <div class="-my-2 overflow-x-auto sm:-mx-6 lg:-mx-8">
                  <div
                    class="
                      py-2
                      align-middle
                      inline-block
                      min-w-full
                      sm:px-6
                      lg:px-8
                    "
                  >
                    <div
                      class="
                        shadow
                        overflow-hidden
                        border-b border-gray-200
                        sm:rounded-lg
                      "
                    >
                      <table
                        class="min-w-full divide-y divide-gray-200"
                      >
                        <thead class="bg-gray-50">
                          <tr>
                            <th
                              scope="col"
                              class="
                                px-6
                                py-3
                                text-left text-xs
                                font-medium
                                text-gray-500
                                uppercase
                                tracking-wider
                              "
                            >
                              Name
                            </th>
                            <th
                              scope="col"
                              class="
                                px-6
                                py-3
                                text-left text-xs
                                font-medium
                                text-gray-500
                                uppercase
                                tracking-wider
                              "
                            >
                              Nid
                            </th>
                            <th
                              scope="col"
                              class="
                                px-6
                                py-3
                                text-left text-xs
                                font-medium
                                text-gray-500
                                uppercase
                                tracking-wider
                              "
                            >
                              Status
                            </th>
                            <th
                              scope="col"
                              class="
                                px-6
                                py-3
                                text-left text-xs
                                font-medium
                                text-gray-500
                                uppercase
                                tracking-wider
                              "
                            >
                              Role
                            </th>
                          </tr>
                        </thead>
                        <tbody class="bg-white divide-y divide-gray-200">
                          <tr
                            v-for="stat in regStatus"
                            :key="stat.id"
                            :value="stat.id"
                          >
                            <td class="px-6 py-4 whitespace-nowrap">
                              <div class="text-sm text-gray-900">
                                {{ stat.name }}
                              </div>
                            </td>
                            <td class="px-6 py-4 whitespace-nowrap">
                              <div class="text-sm text-gray-900">
                                {{ stat.id_no }}
                              </div>
                            </td>
                            <td
                              v-if="stat.id_no == true"
                              class="px-6 py-4 whitespace-nowrap"
                            >
                              <span
                                class="
                                  px-2
                                  inline-flex
                                  text-xs
                                  leading-5
                                  font-semibold
                                  rounded-full
                                  bg-green-100
                                  text-green-800
                                "
                              >
                                Registered
                              </span>
                            </td>
                            <td
                              class="
                                px-6
                                py-4
                                whitespace-nowrap
                                text-sm text-gray-500
                              "
                            >
                              Admin
                            </td>
                          </tr>

                          <!-- More people... -->
                        </tbody>
                      </table>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
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
      allData: "",
      regStatus: [],
      categories: [],
      divisions: [],
      districts: [],
      upazilas: [],
      centers: [],
      smsVerified: false,
      step: "step_1",
      peopleData: [],
      verifyData: {
        category_id: "",
        id_no: "",
        dob: "",
      },
      division_id: "",
      district_id: "",
      upazila_id: "",
      center_id: "",
      name: "",
      diabates: "",
      phone_no: "",
      verify_code: "",
      smsSent: false,
    };
  },
  mounted() {
    this.getAvailableCategories();
    this.getAvailableDivisions();
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
        if (res.data.success) {
          this.step = "step_2";
        }
      });
    },

    getAvailableDivisions() {
      this.$axios.get("/divisions").then((res) => {
        this.divisions = res.data;
      });
    },

    getAvailableDistricts() {
      this.$axios
        .get("/districts?division_id=" + this.division_id)
        .then((res) => {
          this.districts = res.data;
        });
    },

    getAvailableUpazilas() {
      this.$axios
        .get("/upazilas?district_id=" + this.district_id)
        .then((res) => {
          this.upazilas = res.data;
        });
    },

    getAvailableCenters() {
      this.$axios
        .get("/vaccination-centers?upazila_id=" + this.upazila_id)
        .then((res) => {
          this.centers = res.data;
        });
    },

    goToStepThree() {
      this.step = "step_3";
    },

    sendVerificationSMS() {
      this.$axios
        .post("/phone-verify", {
          phone: this.phone_no,
        })
        .then((res) => {
          if (res.data == "pending") {
            this.smsSent = true;
          }
        });
    },

    verifyCode() {
      this.$axios
        .post("/phone-verify-code", {
          phone: this.phone_no,
          verify_code: this.verify_code,
        })
        .then((res) => {
          if (res.data == "approved") {
            this.smsVerified = true;
            this.step = "step_4";
          }
          console.log(res.data);
        });
    },

    registerPeople() {
      this.allData = {
        category_id: this.verifyData.category_id,
        id_no: this.verifyData.id_no,
        dob: this.verifyData.dob,
        division_id: this.division_id,
        district_id: this.district_id,
        upazila_id: this.upazila_id,
        center_id: this.center_id,
        name: this.name,
        diabates: this.diabates,
        phone_no: this.phone_no,
      };
      this.$axios.post("/register-vaccine", this.allData).then((res) => {
        console.log(res.data);
      });
      console.log(this.allData);
      // this.$axios.post('/register', {
      //   name: this.name,
      //   category_id: this.category_id,
      //   id_no: this.id_no,
      //   dob: this.dob,
      //   diabates: this.diabates,
      //   phone_no: this.phone_no,
      //   center_id: this.center_id
      // }).then(res => {
      //   console.log(res.data)
      // })
    },

    getRegStatus() {
      this.$axios
        .post("/registration-status", { id_no: this.verifyData.id_no })
        .then((res) => {
          this.step = "step_5";
          this.regStatus = res.data;
          console.log(res.data);
        });
    },
  },
};
</script>

<style>
</style>