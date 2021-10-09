<template>
    <div class="ticket__socks_into">
        <div class="ticket__socks_into-title Nunito-Bold">
            Носки в наборе
        </div>
        <div class="ticket__socks_into-wrapper">
            <div v-for="i of socks" :key="i" class="ticket__socks_into-item">
                <img v-bind:src="i"/>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props:['socks'],
    }
</script>

<style>
.ticket__socks_into{
    margin-top: 15px;
}
.ticket__socks_into-title{
    font-size: 14px;
    line-height: 19px;
    color: #000000;
}
.ticket__socks_into-wrapper{
    display: inline-flex;
    flex-wrap: wrap;
    gap: 9px;
    margin-top: 5px;
}
</style>