<template>
  <SignupForm :post="post" :submitSignupForm="signUser" />
</template>

<script>

import SignupForm from '../components/SignupForm.vue'
import { reactive } from 'vue';
//import { useRouter } from 'vue-router';
export default {
  components: {
    SignupForm,
  },
  setup() {

    const API_URL = 'http://localhost:4001/register'
    //const router = useRouter()

    const post = reactive({
      first_name: '',
      last_name: '',
      email: '',
      password: '',
    })

    async function signUser() {
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
      signUser,
    }
  }
}

</script>


<style></style>
