<template>
    <div class="container mt-5">
        <form @submit="submitSignupForm">
            <div class="field">
                <label class="label">Name</label>
                <div class="control">
                    <input v-model="post.first_name" class="input" type="text" placeholder="...">
                </div>
            </div>

            <div class="field">
                <label class="label">Lastname</label>
                <div class="control">
                    <input v-model="post.last_name" class="input" type="text" placeholder="...">
                </div>
            </div>

            <div class="field">
                <label class="label">Email</label>
                <div class="control">
                    <input v-model="post.email" class="input" type="text" placeholder="...">
                </div>
            </div>

            <div class="field">
                <label class="label">Password</label>
                <div class="control">
                    <input v-model="post.password" class="input" type="text" placeholder="...">
                </div>
            </div>


            <div class="field is-grouped">
                <div class="control">
                    <button type="submit" @submit="const preventDefault = __VLS_ctx.preventDefault;
preventDefault()" class="button is-primary" href="http://localhost:8080/">Submit</button>
                </div>
            </div>
        </form>
    </div>
</template>
   
<script>
export default {
    props: ['post', 'submitSignupForm'],
}

</script>
   
   
<style></style>
   