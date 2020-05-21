<template lang="pug">
div
  p.bg-green-200 版型二
  .flex
    aside 側欄行事曆
    button.bg-blue-500.text-white.py-2.px-4.rounded(@click="addNumber()" type="button") 點擊
    .container.mx-auto
      p 點擊次數：{{ $store.state.counter }}
      header
        nav.flex.items-center.justify-between.flex-wrap.bg-teal-500.p-6
          div(class="w-full block flex-grow lg:flex lg:items-center lg:w-auto")
            div(class="text-sm lg:flex-grow")
              a(href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4") 常用功能
              a(href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4") 常用報表
              a(href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4") 功能導覽
              a(href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4") 系統首頁
      nuxt
      footer.text-center
        p.text-sm 瑞友資訊股份有限公司
        p.text-sm Copyright &copy; {{ new Date().getFullYear() }}【RUI-YOU】All Rights Reserved.
</template>

<style lang="sass" scoped>

</style>

<script>
import { mapMutations } from 'vuex'
export default {
  name: 'LayoutTLCA',
  methods: {
    addNumber (e) {
      this.increment()
    },
    ...mapMutations([
      'increment'
    ])
  }
}
</script>
