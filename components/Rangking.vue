<template>
      <div class="flex font-overpass flex-col bg-amber-700 rounded-2xl py-6 px-6 backgroundKotak w-[390px]">
        <div class="flex mb-5">
          <div class="p-3.5 backgroundStar rounded-full">
            <img class="h-3" src="images/icon-star.svg">
          </div>
        </div>
        <div class="title mb-1.5">
          <span class="text-[24px] text-white font-[700]">How did we do?</span>
        </div>
        <div class="message mb-5">
          <span class="text-[15px] font-[400] text-LightGrey">
            Please le us know how we did with your support request. All feedback is appreciated to help us improve our offering
          </span>
        </div>
        <div class="score flex justify-between mb-6">
          <div @click="klik(1)">
            <div
              class="flex justify-center items-center h-[45px] w-[45px] backgroundStar hover:bg-Orange text-MediumGrey hover:text-White rounded-full cursor-pointer"
              v-if="number !=1"
            >
              <span class="pt-1 text-[13px]">1</span>
            </div>
            <div
              class="flex justify-center items-center h-[45px] w-[45px] bg-MediumGrey hover:bg-Orange text-White hover:text-White rounded-full cursor-pointer"
              v-else-if="number=1"
            >
              <span class="pt-1 text-[13px]">1</span>
            </div>
          </div>
          <div @click="klik(2)">
            <div
              class="flex justify-center items-center h-[45px] w-[45px] backgroundStar hover:bg-Orange text-MediumGrey hover:text-White rounded-full cursor-pointer"
              v-if="number !=2"
            >
              <span class="pt-1 text-[13px]">2</span>
            </div>
            <div
              class="flex justify-center items-center h-[45px] w-[45px] bg-MediumGrey hover:bg-Orange text-White hover:text-White rounded-full cursor-pointer"
              v-else-if="number=2"
            >
              <span class="pt-1 text-[13px]">2</span>
            </div>
          </div>
          <div @click="klik(3)">
            <div
              class="flex justify-center items-center h-[45px] w-[45px] backgroundStar hover:bg-Orange text-MediumGrey hover:text-White rounded-full cursor-pointer"
              v-if="number !=3"
            >
              <span class="pt-1 text-[13px]">3</span>
            </div>
            <div
              class="flex justify-center items-center h-[45px] w-[45px] bg-MediumGrey hover:bg-Orange text-White hover:text-White rounded-full cursor-pointer"
              v-else-if="number=3"
            >
              <span class="pt-1 text-[13px]">3</span>
            </div>
          </div>
          <div @click="klik(4)">
            <div
              class="flex justify-center items-center h-[45px] w-[45px] backgroundStar hover:bg-Orange text-MediumGrey hover:text-White rounded-full cursor-pointer"
              v-if="number !=4"
            >
              <span class="pt-1 text-[13px]">4</span>
            </div>
            <div
              class="flex justify-center items-center h-[45px] w-[45px] bg-MediumGrey hover:bg-Orange text-White hover:text-White rounded-full cursor-pointer"
              v-else-if="number=4"
            >
              <span class="pt-1 text-[13px]">4</span>
            </div>
          </div>
          <div @click="klik(5)">
            <div
              class="flex justify-center items-center h-[45px] w-[45px] backgroundStar hover:bg-Orange text-MediumGrey hover:text-White rounded-full cursor-pointer"
              v-if="number !=5"
            >
              <span class="pt-1 text-[13px]">5</span>
            </div>
            <div
              class="flex justify-center items-center h-[45px] w-[45px] bg-MediumGrey hover:bg-Orange text-White hover:text-White rounded-full cursor-pointer"
              v-else-if="number=5"
            >
              <span class="pt-1 text-[13px]">5</span>
            </div>
          </div>
        </div>
        <button @click="sendValues" class="btnSubmit text-center bg-Orange hover:bg-White text-White hover:text-Orange rounded-2xl py-2">
          <span class=" text-[14px] font-[700]">SUBMIT</span>
        </button>
      </div>
</template>
<script lang="js">
import Resume from "./Resume";
export default {
  components: {Resume},
  data() {
    return {
      number: 0,
      click: false,
      hasSubmit: false
    }
  },
  methods: {
    klik(x = 0) {
      this.click = !this.click
      this.number = x
      return this.number
    },
    sendValues(){
      if (this.number !== 0)
      this.hasSubmit = true
      this.$emit("sendValue",this.hasSubmit)
      this.$emit("sendRank",this.number)
    }
  },
  computed: {
    colorSelect() {
      return this.number !== 0 ? 'MediumGrey' : 'backgroundStar'
    }
  }
}
</script>
