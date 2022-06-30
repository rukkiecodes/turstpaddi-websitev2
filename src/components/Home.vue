<script setup>
import Slider from "./Slider.vue"
import { useWaitlistStore } from '../store/waitlist'

const buyer = true

const waitlist = useWaitlistStore()
</script>


<template>
  <section
    class="lg:mx-32 mx-8 lg:flex justify-evenly mt-32"
    data-aos="fade-down"
  >
    <div class="lg:text-left text-center">
      <div class="
          lg:w-3/4 lg:leading-relaxed
          font-bold
          text-blue
        ">
        <p>coming soon 🚀🚀🚀</p>
        <p class="lg:text-4xl text-4xl mt-5">Get Notified</p>
        <p class="lg:text-4xl text-4gl">When we Launch🚀</p>
      </div>
      <p class="text-sm lg:w-4/5 my-8">
        Transact Securely with online vendors & marketplaces, gain customers
        trust with TrustPaddi
      </p>
      <div class="flex justify-between items-center">
        <div class="flex flex-1 rounded-md shadow-sm mr-2">
          <input
            type="text"
            v-model="waitlist.email"
            @keypress.enter="waitlist.sendNewWait"
            class="focus:ring-indigo-500 focus:border-indigo-500 flex-1 block w-full rounded-md sm:text-sm border-gray-300"
            placeholder="Enter your email"
          />
        </div>
        <button
          @click="waitlist.sendNewWait"
          class="p-2 rounded-lg bg-blue"
          style="color: #fff"
        >{{ waitlist.loading == true ? 'Loading...' : 'Notify Me' }}</button>
      </div>
      <p v-show="waitlist.snack" class="font-bold text-sm" style="color: green">{{ text }}</p>
    </div>
    <div class="lg:w-3/5 lg:my-0 my-8">
      <img
        class="w-screen"
        src="../assets/man-with-phone.png"
        alt=""
      />
    </div>
  </section>
  <section class="py-20 lg:px-28 linear">
    <div class="text-3xl font-bold text-center mt-5 text-blue">
      Introducing Trustpaddi
    </div>
    <p class="text-center text-xs text-gray">
      The safest and surest way to transact
    </p>
    <div class="lg:flex mt-16">
      <div class="w-80 m-8">
        <img
          src="../assets/icons/pay-dollar.png"
          alt=""
        />
        <div class="text-lg font-bold my-3 text-blue">Escrow Payment</div>
        <div class="text-gray">
          We offer an escrow payment platform that bridge the trust issues
          between sellers and there potential online customers
        </div>
      </div>
      <div class="w-80 m-8">
        <img
          src="../assets/icons/dashboard.png"
          alt=""
        />
        <div class="text-lg font-bold my-3 text-blue">
          Order Management System
        </div>
        <div class="text-gray">
          We have an order management system, order fulfilment system and sales
          tracking system all in one platform to make online selling easy and
          stress-free.
        </div>
      </div>
      <div class="w-80 m-8">
        <img
          src="../assets/icons/pay-dollar.png"
          alt=""
        />
        <div class="text-lg font-bold my-3 text-blue">No Cash Risk</div>
        <div class="text-gray">
          An easier solution for sellers to make sales to prospective buyers
          outside there reach (States) without having to deal with the risk
          associated with cash on delivery
        </div>
      </div>
    </div>
    <div class="mx-auto lg:w-2/5 w-3/5 mt-10">
      <img
        src="../assets/celebration.png"
        alt=""
      />
    </div>
  </section>
</template>

<style>
.linear {
  background: linear-gradient(
    181.9deg,
    #f4f0ff 64.77%,
    rgba(244, 240, 255, 0) 101.34%
  );
}
.works {
  background: linear-gradient(
    6.24deg,
    #fef9f1 76.75%,
    rgba(255, 255, 255, 0.74) 99.26%
  );
}
.safe {
  background: linear-gradient(
    99.01deg,
    #dbccff 32.52%,
    rgba(219, 204, 255, 0.63) 48.95%,
    rgba(250, 214, 158, 0.2) 63.34%,
    rgba(250, 214, 158, 0.3) 79.39%
  );
}
.testimonials {
  background: url("../assets/map.png");
}
</style>
