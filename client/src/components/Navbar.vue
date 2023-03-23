<template>
 <nav class="navbar" role="navigation" aria-label="main navigation" color="blue">
  <div class="navbar-brand">
    <a class="navbar-item" href="">
      <img src="https://jwt.io/img/icon.svg" width="200" height="200">
    </a>

    <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>

  <div id="navbarBasicExample" class="navbar-menu">
    <div class="navbar-start">
      <a class="navbar-item">
        
      </a>

      <a class="navbar-item">
        <h1>Json Web Token</h1>
      </a>

      
    </div>

    <div class="navbar-end">
      <div class="navbar-item">
        <div class="buttons">
          <RouterLink to="/signup" class="button is-primary">
            <strong>Sign up</strong>
          </RouterLink>
          <RouterLink to="/login" class="button is-light">
            Log in
          </RouterLink>
        </div>
      </div>
    </div>
  </div>
</nav>
</template>

<script>

</script>


<style>

</style>