<template lang="pug">
  .bg-gray-200.min-h-screen
    h1.text-center.text-4xl.py-4.mb-8 條件渲染
    .flex.items-center.justify-center.mb-4
      .w-full.max-w-xs(v-if="visible") 區塊A
      .w-full.max-w-xs(v-else) 區塊B
    .flex.items-center.justify-center
      button.bg-blue-500.text-white.font-bold.py-2.px-4.rounded(@click="toggle") 切換
</template>

<script>
export default {
  name: 'Page01DataBinding',
  data () {
    return {
      visible: true
    }
  },
  methods: {
    toggle () {
      this.visible = !this.visible
    }
  }
}
</script>
