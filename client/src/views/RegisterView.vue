<template>
  <Register :post="post" :submitForm="createUser" />
</template>

<script>
import Register from '@/components/Register.vue'
import { onMounted, reactive } from 'vue';


export default {
  components: {
    Register,
  },
  setup() {

    const API_URL = 'http://localhost:4001/register'

    const post = reactive({
      first_name: '',
      last_name: '',
      email: '',
      password: '',
    })

    async function createUser(e) {
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
        const json = await response.json()
        router.push({
          name: 'Home',
        })
      } catch (error) {
        console.log(error)
      }
    }
    return {
      post,
      createUser,
    }
  }
}

</script>
<style></style>