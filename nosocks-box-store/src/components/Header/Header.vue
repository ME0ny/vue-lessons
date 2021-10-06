<template>
    <div>
        <div class="logo">
            <img src="./img/logo.png" class="logo__image" alt="">
            <div class="logo__text">Nosocks</div>
        </div>
        <header-title />
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
                auth: false
            }
        },
        components: {
            "header-title": Header__Title,
            "auth-button": AuthButton
        }
    }
</script>

<style>

</style>
