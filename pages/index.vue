<template lang="pug">
  .container.mx-auto
    ul.flex
      li.mr-6: nuxt-link.text-blue-500(class="hover:text-blue-800" :to="'01-data-binding'" title="資料綁定") 資料綁定
      li.mr-6: nuxt-link.text-blue-500(class="hover:text-blue-800" :to="'02-conditional'" title="條件渲染") 條件渲染
      li.mr-6: nuxt-link.text-blue-500(class="hover:text-blue-800" :to="'03-list'" title="列表渲染") 列表渲染
      li.mr-6: nuxt-link.text-blue-500(class="hover:text-blue-800" :to="{ name: 'tlca' }" title="長照系統") 長照系統
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      links: [{
        href: '01-data-binding'
      }, {
        href: '02-conditional'
      }]
    }
  }
}
</script>
