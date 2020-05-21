<template lang="pug">
  .bg-gray-200.min-h-screen
    h1.text-center.text-4xl.py-4.mb-8 列表渲染
    .flex.items-center.justify-center
      .w-full.max-w-xs 區塊A
      .w-full.max-w-xs 區塊B
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
