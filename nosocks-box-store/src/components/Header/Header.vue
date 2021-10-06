<template>
    <div class="wrapper">
        <div class="logo">
            <img src="./img/logo.png" class="logo__image" alt="">
            <div class="logo__text">Nosocks</div>
        </div>
        <header-title 
            v-bind:header_title="header_title"/>
        <auth-button 
            v-bind:auth="auth"/>
    </div>
</template>

<script>
    import Header__Title from "@/components/Header_Title/Header__Title"
    import AuthButton from "@/components/AuthButton/AuthButton"
    export default {
        data() {
            return {
                auth: false,
                header_title: {
                    title: "Наборы носков",
                    description: `Ты можешь заказать существующие наборы или принять
участие в сборе средств на новый набор`
                }
            }
        },
        components: {
            "header-title": Header__Title,
            "auth-button": AuthButton
        }
    }
</script>

<style>
@font-face {
font-family: "Nunito";
src: local("Nunito"),
   url(./fonts/Nunito-Regular.ttf) format("truetype");
}
.wrapper{
    display: grid;
    grid-template-columns: 119px 3fr 1fr;
}

.logo{
    margin-left: 46px;
}

.logo__image{
    width: 66px;
    height: 66px;
}

.logo__text{
    font-family: "Nunito";
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 25px;
    /* identical to box height */
    padding: auto;
}


</style>
