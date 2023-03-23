<template>
    <LoginForm :post="post" :submitLoginForm="createUser" />
</template>

<script>
import LoginForm from '../components/LoginForm.vue'
import { reactive } from 'vue';
import { useRouter } from 'vue-router';
export default {
    components: {
        LoginForm,
    },

    
    

    
}



</script>


<style></style>
