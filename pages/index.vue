<template>
  <div class="relative">
    <div class="primary-bg pt-2 pb-24">
      <div class="container mx-auto">
        <div class="flex items-center">
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
              <input type="text" class="w-full ml-1 -mr-20 -mt-2 rounded-3xl" />
              <button class="w-1/6 -mt-1 my-1 primary-bg rounded-3xl -mr-1">
                Go
              </button>
            </div>
          </div>
          <div class="min-w-max">
            <img src="~/static/img/hero.png" alt="" />
          </div>
        </div>
      </div>
    </div>
    <div class="container small-cntainer text-center mx-auto mt-16">
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

    <div class="container mx-auto mt-36">
      <div class="primary-bg text-white mx-auto rounded-3xl py-20 px-16">
        <div class="flex items-center">
          <div class="w-1/3 mr-10 font-bold">
            <h1 class="text-7xl uppercase">Hotline</h1>
            <p class="text-4xl">Numbers</p>
          </div>
          <div class="w-2/3">
            <div class="flex flex-wrap -mx-8">
              <div class="w-1/2 px-8 mb-8">
                <div class="bg-white rounded-xl p-4 text-black">
                  <div class="flex items-center">
                    <div class="min-w-max mr-3">
                      <img src="~/static/img/phone-call-pink.svg" alt="" />
                    </div>
                    <div class="w-full">
                      <h1 class="text-3xl font-bold text-pink-500">333</h1>
                      <p class="text-xl font-normal text-black">
                        National Call Center
                      </p>
                    </div>
                  </div>
                </div>
              </div>
              <div class="w-1/2 px-8 mb-8">
                <div class="bg-white rounded-xl p-4 text-black">
                  <div class="flex items-center">
                    <div class="min-w-max mr-3">
                      <img src="~/static/img/phone-call-green.svg" alt="" />
                    </div>
                    <div class="w-full">
                      <h1 class="text-3xl font-bold text-green-500">16263</h1>
                      <p class="text-xl font-normal text-black">
                        Health Portal
                      </p>
                    </div>
                  </div>
                </div>
              </div>
              <div class="w-1/2 px-8">
                <div class="bg-white rounded-xl p-4 text-black">
                  <div class="flex items-center">
                    <div class="min-w-max mr-3">
                      <img src="~/static/img/phone-call-yellow.svg" alt="" />
                    </div>
                    <div class="w-full">
                      <h1 class="text-3xl font-bold text-yellow-500">10655</h1>
                      <p class="text-xl font-normal text-black">IEDCR</p>
                    </div>
                  </div>
                </div>
              </div>
              <div class="w-1/2 px-8">
                <div class="bg-white rounded-xl p-4 text-black">
                  <div class="flex items-center">
                    <div class="min-w-max mr-3">
                      <img src="~/static/img/phone-call-blue.svg" alt="" />
                    </div>
                    <div class="w-full">
                      <h1 class="text-3xl font-bold text-blue-500">
                        09666777222
                      </h1>
                      <p class="text-xl font-normal text-black">
                        Covid-19 Telehealth
                      </p>
                    </div>
                  </div>
                </div>
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