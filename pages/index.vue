<template>
  <div class="relative mt-60">
    <div class="container small-cntainer text-center mx-auto">
      <div class="top-small-container mx-auto">
        <h2 class="text-4xl text-black mb-6 font-semibold">
          Register for Vaccine
        </h2>
        <p class="text-lg">
          You will just need your NID Card, Phone number and filling up some
          info
        </p>
        <div class="flex mt-20">
          <div class="w-1/3">
            <img class="mx-auto mb-12" src="~/static/img/nid.svg" alt="" />
            <div
              class="mx-auto w-6 h-6 border-4 border-green-400 rounded-full"
            ></div>
            <p class="text-lg font-bold mx-auto mt-5">NID</p>
          </div>

          <div class="w-1/3">
            <img class="mx-auto mb-12" src="~/static/img/phone.svg" alt="" />
            <div
              class="mx-auto w-6 h-6 border-4 border-yellow-400 rounded-full"
            ></div>
            <p class="mx-auto text-lg font-bold mt-5">Phone</p>
          </div>

          <div class="w-1/3">
            <img
              class="mx-auto mb-12"
              src="~/static/img/information.svg"
              alt=""
            />
            <div
              class="mx-auto w-6 h-6 border-4 border-blue-500 rounded-full"
            ></div>
            <p class="mx-auto text-lg font-bold mt-5">Information</p>
          </div>
        </div>
        <div class="text-left w-10/12 mx-auto mt-14">
          <h2 class="text-4xl font-semibold text-black">Get Updates</h2>
          <p class="text-lg font-normal text-black mt-2.5">
            Check Your Registration Status, Vaccine card, Certificate and See
            Faqs .
          </p>
        </div>
        <div class="flex mt-12 box-mid mx-auto">
          <div class="w-1/4 px-5">
            <nuxt-link to="" class="block shadow-lg w-56 h-80 px-14 relative">
              <div class="flex justify-center items-center h-48">
                <img class="" src="~/static/img/004-checkmark1.svg" alt="" />
              </div>
              <p class="font-semibold text-lg pt-11">Check Status</p>
              <div class="absolute bottom-0 -mb-4 left-0 ml-24">
                <img src="~/static/img/ra-pink.svg" alt="" />
              </div>
            </nuxt-link>
          </div>
          <div class="w-1/4 px-4">
            <nuxt-link to="" class="block shadow-lg w-56 h-80 px-14 relative">
              <div class="flex justify-center items-center h-48">
                <img class="" src="~/static/img/005-id-card1.svg" alt="" />
              </div>
              <p class="font-semibold text-lg pt-11">Vaccine card</p>
              <div class="absolute bottom-0 -mb-4 left-0 ml-24">
                <img src="~/static/img/ra-green.svg" alt="" />
              </div>
            </nuxt-link>
          </div>
          <div class="w-1/4 px-4">
            <nuxt-link to="" class="block shadow-lg w-56 h-80 px-14 relative">
              <div class="flex justify-center items-center h-48">
                <img class="" src="~/static/img/008-certificate1.svg" alt="" />
              </div>
              <p class="font-semibold text-lg pt-11">Certificate</p>
              <div class="absolute bottom-0 -mb-4 left-0 ml-24">
                <img src="~/static/img/ra-yellow.svg" alt="" />
              </div>
            </nuxt-link>
          </div>
          <div class="w-1/4 px-4">
            <nuxt-link to="" class="block shadow-lg w-56 h-80 px-14 relative">
              <div class="flex justify-center items-center h-48">
                <img class="" src="~/static/img/011-faq1.svg" alt="" />
              </div>
              <p class="font-semibold text-lg pt-11">FAQs</p>
              <div class="absolute bottom-0 -mb-4 left-0 ml-24">
                <img src="~/static/img/ra-indigo.svg" alt="" />
              </div>
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
    <div class="container mx-auto">
      <div class="mid-small-container mt-36">
        <div class="primary-bg-color mx-auto text-white rounded-3xl p-10">
          <div class="flex">
            <div class="w-1/3">
              <h1 class="text-7xl font-bold uppercase">Hotline</h1>
              <p class="text-4xl font-bold">Numbers</p>
            </div>
            <div class="w-2/3">
              <div class="flex">
                <div class="w-1/2 bg-white rounded-3xl mx-8"></div>
                <div class="w-1/2 bg-white rounded-3xl mx-8"></div>
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
  name: "IndexPage",
};
</script>

        <div class="mid-box2 mx-auto mt-24">
          <div class="flex">
            <img class="mx-auto w-20 h-18" src="~/static/img/nid.svg" alt="" />
            <img class="mx-auto" src="~/static/img/phone.svg" alt="" />
            <img
              class="mx-auto w-20"
              src="~/static/img/information.svg"
              alt=""
            />
          </div>
          <div class="flex mt-8 mx-auto">
            <div
              class="mx-auto w-6 h-6 border-4 border-green-400 rounded-full"
            ></div>
            <div
              class="mx-auto w-6 h-6 border-4 border-yellow-400 rounded-full"
            ></div>
            <div
              class="mx-auto w-6 h-6 border-4 border-blue-500 rounded-full"
            ></div>
          </div>
          <div class="flex mt-4 mx-auto">
            <p class="w-1/3 text-lg font-bold">NID</p>
            <p class="w-1/3 text-lg font-bold">Phone</p>
            <p class="w-1/3 text-lg font-bold">Information</p>
          </div>
        </div>
        <div>
          <div class="mid-box3 text-left mt-14">
            <h2 class="text-4xl font-semibold text-black">Get Updates</h2>
            <p class="text-lg font-normal text-black">
              Check Your Registration Status, Vaccine card, Certificate and See
              Faqs .
            </p>
          </div>
        </div>
        <div class="mid-box4">
          <div class="flex">
            <div class="w-1/4">
              <nuxt-link>
                <img class="w-56 h-80" src="" alt="" />
              </nuxt-link>
            </div>
            <div class="w-1/4">
              <nuxt-link>
                <img class="w-56 h-80" src="" alt="" />
              </nuxt-link>
            </div>
            <div class="w-1/4">
              <nuxt-link>
                <img class="w-56 h-80" src="" alt="" />
              </nuxt-link>
            </div>
            <div class="w-1/4">
              <nuxt-link>
                <img class="w-56 h-80" src="" alt="" />
              </nuxt-link>
            </div>
          </div>
        </div>
