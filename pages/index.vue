<template lang="pug">
  .container.mx-auto
    ul.flex
      li.mr-6: nuxt-link.text-blue-500(class="hover:text-blue-800" :to="'01-data-binding'" title="資料綁定") 資料綁定
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      links: [{
        href: '01-data-binding'
      }]
    }
  }
}
</script>
