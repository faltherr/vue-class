<template>
    <div class="login-main-container">
        <form v-on:submit.prevent="checkLogin">
            <input placeholder="username" v-model="usernameInput"/>
            <input placeholder="password" v-model="passwordInput"/>
            <button type="submit">Login</button>
        </form>
    </div>
</template>

<script>
export default {
    name: 'login',
    data: function() {
        return {
            usernameInput: '',
            passwordInput: ''
        }
    },
    methods: {
        checkLogin: function() {
            if(this.usernameInput && this.passwordInput) {
                this.$router.push({path: '/dashboard'})
            }
        }
    }
}
</script>