<template>
  <div class="font-overpass background min-h-screen">
    <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2">
      <Rangking v-if="!value" @sendValue="receiveVal" @sendRank="receiveRank"></Rangking>
      <Resume v-if="value" :test="rank"></Resume>
    </div>
  </div>
</template>
<script lang="js">
export default {
  data() {
    return {
      value: false,
      rank: 0
    }
  },
  methods: {
    receiveVal(s) {
      this.value = s
    },
    receiveRank(x){
      this.rank=x
    }
  }
}
</script>
