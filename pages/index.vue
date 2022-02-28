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
            <div class="flex rounded-full bg-white items-center p-1 w-2/3">
              <input type="text" class="w-full px-3 focus:outline-none" />
              <button
                class="
                  min-w-max
                  primary-bg
                  text-base
                  font-medium
                  rounded-full
                  px-6
                  py-2
                  -m-px
                  text-white
                "
              >
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

    <div class="relative">
      <div class="dots-1 left-20 top-20 absolute"></div>
      <div class="ellipse absolute right-0 top-0"></div>
      <div class="container mx-auto small-container text-center pt-20">
        <div>
          <div class="text-center">
            <h2 class="text-4xl text-black mb-6 font-semibold">
              Register for Vaccine
            </h2>
            <p class="text-lg">
              You will just need your NID Card, Phone number and filling up some
              info
            </p>
          </div>
        </div>
      </div>
    </div>

    <div class="relative">
      <div class="container mx-auto small-container text-center">
        <div>
          <div class="max-w-screen-sm mx-auto">
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
                  <img class="mx-auto" src="~/static/img/phone.svg" alt="" />
                </div>
                <div
                  class="
                    border-4
                    w-6
                    h-6
                    rounded-full
                    mx-auto
                    mb-4
                    mt-8
                    tika-step
                    relative
                  "
                ></div>
                <p class="text-lg font-bold">Phone</p>
              </div>

              <div class="flex-1 px-6">
                <div class="h-32 flex justify-center items-center">
                  <img
                    class="mx-auto"
                    src="~/static/img/information.svg"
                    alt=""
                  />
                </div>
                <div
                  class="
                    border-4
                    w-6
                    h-6
                    rounded-full
                    mx-auto
                    mb-4
                    mt-8
                    tika-step
                    relative
                  "
                ></div>
                <p class="text-lg font-bold">Information</p>
              </div>
            </div>
          </div>

          <div class="text-left mb-16">
            <div class="dots-2 right-64 top-56 absolute"></div>
            <h2 class="text-4xl font-bold mb-6">Get Updates</h2>
            <p class="text-lg">
              Check Your Registration Status, Vaccine card, Certificate and See
              Faqs .
            </p>
          </div>

          <div class="flex mt-10 mb-40 mx-auto">
            <div class="w-1/4 px-2">
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
            <div class="w-1/4 px-2">
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
            <div class="w-1/4 px-2">
              <nuxt-link to="" class="block shadow-lg w-56 h-80 px-14 relative">
                <div class="flex justify-center items-center h-48">
                  <img
                    class=""
                    src="~/static/img/008-certificate1.svg"
                    alt=""
                  />
                </div>
                <p class="font-semibold text-lg pt-11">Certificate</p>
                <div class="absolute bottom-0 -mb-4 left-0 ml-24">
                  <img src="~/static/img/ra-yellow.svg" alt="" />
                </div>
              </nuxt-link>
            </div>
            <div class="w-1/4 px-2">
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
            <div class="dots-3 -bottom-28 left-20 absolute"></div>
          </div>
        </div>
      </div>
    </div>

    <!-- Bottom Counter -->
    <div class="relative">
      <!-- <div class="absolute ellipse-full left-1/4 top-1/5"></div> -->
      <div class="container mx-auto">
        <div
          class="primary-bg text-white mx-auto mb-52 rounded-3xl py-20 px-16"
        >
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
                        <h1 class="text-3xl font-bold text-yellow-500">
                          10655
                        </h1>
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
      <div class="dots-2 left-20 -bottom-32 absolute"></div>
      <div class="absolute ellipse-full right-40 -bottom-64"></div>
    </div>

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

    <div class="primary-bg text-center text-white text-2xl font-bold py-20">
      <div class="container mx-auto">
        <div class="flex">
          <div class="flex-1 px-10">
            <h3 class="font-bold text-5xl mb-4">10,000,000</h3>
            <p>Registered</p>
          </div>

          <div class="flex-1 px-10">
            <h3 class="font-bold text-5xl mb-4">8,000,000</h3>
            <p>Vaccinated</p>
          </div>

          <div class="flex-1 px-10">
            <h3 class="font-bold text-5xl mb-4">7,000,000</h3>
            <p>Certificate Issued</p>
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