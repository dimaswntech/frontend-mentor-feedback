<template>
  <div class="flex flex-col items-center font-overpass bg-amber-700 rounded-2xl py-10 px-6 backgroundKotak w-[390px]">
    <div class="imageThanks mb-8">
      <img class="h-[100px]" src="images/illustration-thank-you.svg">
    </div>
    <div class="rankChoose px-4 mb-8 text-center backgroundStar rounded-2xl">
      <span class="text-Orange text-[15px]">You selected {{ test }} of 5</span>
    </div>
    <div class="textThanks text-center mb-2">
      <span class="text-[24px] text-white font-[700]">Thank you!</span>
    </div>
    <div class="textOk text-center">
      <span class="text-[15px] font-[400] text-LightGrey">We appreciate you taking the time to give a rating. If You ever need more support, don't hestitate to get in touch!</span>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    test: {
      type: Number
    }
  },
  data() {
    return {
      //value: this.props.test
    }
  },
}
</script>
