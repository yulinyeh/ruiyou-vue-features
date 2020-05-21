<template lang="pug">
div
  p 首頁
  p 本地：{{ counter }}
  button.bg-blue-500.text-white.py-2.px-4.rounded(@click="addNumber()" type="button") 點擊
  button.bg-blue-500.text-white.py-2.px-4.rounded(@click="aad()") 本地
</template>

<style lang="sass" scoped>
</style>

<script>
import { mapMutations } from 'vuex'
export default {
  name: 'PageTlcaIndex',
  layout: 'tlca',
  data () {
    return {
      counter: 0
    }
  },
  methods: {
    addNumber (e) {
      console.log(this.$store.state.counter)
      this.increment()
    },
    aad (e) {
      this.counter++
      this.increment()
    },
    ...mapMutations([
      'increment'
    ])
  }
}
</script>
