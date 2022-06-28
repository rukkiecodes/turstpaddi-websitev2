<script setup>
import Slider from "./Slider.vue"
import { useWaitlistStore } from '../store/waitlist'

const buyer = true

const waitlist = useWaitlistStore()


// export default {
//   data () {
//     return {
//       buyer: true,
//     };
//   },
//   methods: {
//     ...mapActions(useWaitlistStore, ["sendNewWait"]),

//     toggleBuyer () {
//       this.buyer = !this.buyer;
//     },
//   },
//   components: { Slider },

//   computed: {
//     ...mapState(useWaitlistStore, ["email", "loading", "snack", "text"])
//   }
// };
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
  <section class="bg-who lg:px-32 py-20 relative">
    <div class="text-3xl text-bold text-center text-white my-3">
      Who can use Trustpaddi
    </div>
    <img
      src="../assets/mocups/who-top.png"
      class="absolute top-0 left-0"
      alt=""
    />
    <img
      src="../assets/mocups/footer-bottom.png"
      class="absolute bottom-0 right-0"
      alt=""
    />

    <div class="lg:flex my-8">
      <div class="m-5 lg:my-0 my-10 text-white lg:w-1/2">
        <div class="text-dark-orange text-xs">INDIVIDUALS</div>
        <div class="text-xl text-white font-bold my-1">Peer 2 Peer</div>
        <div class="my-3 lg:text-sm text-base">
          Anyone can use TrustPaddi especially when it comes to making
          transactions with unknown online vendors, service providers or with
          people whom you haven't done business with before.
        </div>
      </div>
      <div class="m-5 lg:my-0 my-10 text-white lg:w-1/2">
        <div class="text-dark-orange text-xs">BUSINESSES</div>
        <div class="text-xl text-white font-bold my-1">Sellers and Vendors</div>
        <div class="my-3 lg:text-sm text-base">
          Any Business owner can use TrustPaddi, with our escrow services you
          can gain the Trust and Reliability that big brands enjoy, boost your
          sales, avoid the risk associated with cash on delivery (COD), attend
          to as much order as you want and enjoy peace of mind knowing you will
          get paid instantly without stories.
        </div>
      </div>
      <div class="m-5 lg:my-0 my-10 text-white lg:w-1/2">
        <div class="text-dark-orange text-xs">E-COMMERCE</div>
        <div class="text-xl text-white font-bold my-1">Online marketplaces</div>
        <div class="my-3 lg:text-sm text-base">
          Any Business owner can use TrustPaddi, with our escrow services you
          can gain the Trust and Reliability that big brands enjoy, boost your
          sales, avoid the risk associated with cash on delivery (COD), attend
          to as much order as you want and enjoy peace of mind knowing you will
          get paid instantly without stories.
        </div>
      </div>
    </div>
    <div class="text-center">
      <input
        type="button"
        value="Get Started"
        class="p-3 bg-white rounded-3xl px-16 text-blue"
      />
    </div>
  </section>
  <section class="my-24 testimonials mx-auto lg:w-9/12">
    <Slider />
  </section>
  <section>
    <div class="lg:w-8/12 p-8 rounded-3xl mx-auto safe">
      <div class="text-3xl font-bold text-center my-5 text-blue">
        Better safe than sorry
      </div>
      <div class="text-center">
        <input
          type="button"
          value="Get Started"
          class="p-3 bg-blue rounded-3xl px-16 text-white"
        />
      </div>
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
