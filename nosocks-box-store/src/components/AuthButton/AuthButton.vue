<template>
    <div>
        <div v-if="auth == true" class="button button_account">
            <img src="./img/account.png" alt="">
        </div>
        <div v-else style="width: 100%;">
            <button class="button button_sign_in">
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
@font-face {
font-family: "Nunito";
    src: local("Nunito"),
   url(./fonts/Nunito-Regular.ttf) format("truetype");
}
.button_sign_in{
    font-family: "Nunito";
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 25px;

    width: 80px;
    height: 30px;
    background: #FFE600;
    border: #FFE600;
    float:right;
}
</style>