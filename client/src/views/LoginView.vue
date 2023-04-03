<template>
  <Login :post="post" :submitForm="loginUser" />
</template>

<script>
import Login from '@/components/Login.vue'
import { reactive } from 'vue';
import { useRouter } from 'vue-router';
import axios from 'axios';

export default {
  components: {
    Login,
  },
  setup() {
    const API_URL = 'http://localhost:4001/login'

    const post = reactive({
      first_name: '',
      last_name: '',
      email: '',
      password: '',
    })

    async function loginUser(e) {
      e.preventDefault()
      try {
        const response = await fetch(API_URL, {
          method: 'POST',
          headers: {
            'content-type': 'application/json'
          },
          body: JSON.stringify({
            first_name: post.first_name,
            last_name: post.last_name,
            email: post.email,
            password: post.password
          })
        })
      } catch (error) {
        console.log(error)
      }
    }
    return {
      post,
      loginUser,
    }
}}
</script>
<style>
</style>