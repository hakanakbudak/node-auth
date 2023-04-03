<template>
  <div class="container mt-5">
      <form @submit.prevent="loginForm">
          <div class="field">
              <label class="label">Firstname</label>
              <div class="control">
                  <input v-model="post.email" class="input" type="text" placeholder="...">
              </div>
          </div>

          <div class="field">
              <label class="label">Lastname</label>
              <div class="control">
                  <input v-model="post.password" class="input" type="text" placeholder="...">
              </div>
          </div>

          <div class="field is-grouped">
              <div class="control">
                  <button type="submit" class="button is-primary" href="http://localhost:8080/">Login</button>
              </div>
          </div>
      </form>
  </div>
</template>

<script>
export default {
  props: ['post', 'loginForm'],
}

</script>

<style></style>