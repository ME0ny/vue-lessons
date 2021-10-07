<template>
    <div>
        <div v-if="auth == true" class="button button_account">
            <img src="./img/account.png" alt="">
        </div>
        <div v-else style="width: 100%;">
            <button class="button button_sign_in Nunito-Regular">
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

<style>
.button_sign_in{
    font-size: 1.4rem;
    line-height: 25px;

    width: 80px;
    height: 30px;
    background: #FFE600;
    border: #FFE600;
    float:right;
}
</style>