<template>
    <nav class="navbar" role="navigation" aria-label="main navigation">
        <div class="navbar-brand">
            <a class="navbar-item" href="https://bulma.io">
                <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28">
            </a>
        </div>

        <div>

            <div class="navbar-end">
                <div class="navbar-item">
                    <div class="buttons">
                        <RouterLink to="/register" class="button is-primary">
                            <strong>Register</strong>
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


<style></style>