<template lang="pug">
  .bg-gray-200.min-h-screen
    h1.text-center.text-4xl.py-4.mb-8 雙向綁定
    .flex.items-center.justify-center
      .w-full.max-w-xs.mr-8
        form.bg-white.shadow-md.rounded.px-8.pt-6.pb-8.mb-4
          .mb-4
            label.block.text-gray-700.text-sm.font-bold.mb-2(for='username') Username
            input#username.shadow.appearance-none.border.rounded.w-full.py-2.px-3.text-gray-700.leading-tight(v-model.trim="form.username" class='focus:outline-none focus:shadow-outline' type='text' placeholder='Username')
          .mb-6
            label.block.text-gray-700.text-sm.font-bold.mb-2(for='password') Password
            input#password.shadow.appearance-none.border.rounded.w-full.py-2.px-3.text-gray-700.mb-3.leading-tight(v-model.trim="form.password" class='focus:outline-none focus:shadow-outline' type='password' placeholder='******************')
          .flex.items-center.justify-between
            button.bg-blue-500.text-white.font-bold.py-2.px-4.rounded(@click="submit" class='hover:bg-blue-700 focus:outline-none focus:shadow-outline' type='button') Sign In
            a.inline-block.align-baseline.font-bold.text-sm.text-blue-500(class='hover:text-blue-800' href='#') Forgot Password?
        p.text-center.text-gray-500.text-xs &copy;2020 Acme Corp. All rights reserved.
      .w-full.max-w-xs
        .bg-white.shadow-md.rounded.px-8.pt-6.pb-8
          pre.text-gray-700.leading-tight {{ form }}
</template>

<script>
export default {
  name: 'Page01DataBinding',
  data () {
    return {
      form: {
        username: '',
        password: ''
      }
    }
  },
  methods: {
    submit () {
      alert(JSON.stringify(this.form))
    }
  }
}
</script>
