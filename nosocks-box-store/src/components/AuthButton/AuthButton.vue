<template>
    <div>
        <div v-if="auth == true" class="button button_sign_in">
            <img src="./img/account.png" alt="">
        </div>
        <div v-else class="button button_account">
            <button class="button">
                Войти
            </button>
        </div>
    </div>
</template>

<script>
    export default {
        props:  ["auth"]
    }
</script>