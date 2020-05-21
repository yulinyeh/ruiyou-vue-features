<template lang="pug">
  .bg-gray-200.min-h-screen
    h1.text-center.text-4xl.py-4.mb-8 雙向綁定
    .flex.items-center.justify-center
      .w-full.max-w-xs.mr-8
        form
          .mb-4
            label(for='username') Username
            input(v-model.trim="form.username" class='focus:outline-none focus:shadow-outline' type='text' placeholder='Username')
          .mb-6
            label(for='password') Password
            input(v-model.trim="form.password" class='focus:outline-none focus:shadow-outline' type='password' placeholder='******************')
          .flex.items-center.justify-between
            button(@click="submit" class='hover:bg-blue-700 focus:outline-none focus:shadow-outline' type='button') Sign In
            a(class='hover:text-blue-800' href='#') Forgot Password?
        p &copy;2020 Acme Corp. All rights reserved.
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
        username: 'aaa',
        password: 'vvv'
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
