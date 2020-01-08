<template>
  <q-page class="flex flex-center">
    <div class="row">
      <div class="col">
        <q-input filled v-model="username" label="Your Name"/>
        <br>
        <q-input filled type="password" v-model="password" label="Your Password"/>
        <br>
        <q-btn label="Login" color="primary" @click="doLogin"/>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'Login',
  data () {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    doLogin () {
      this.$router.push({
        path: '/index'
      })
    }
  }
}
</script>
