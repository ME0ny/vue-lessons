<template>
    <div class="title">
        <div class="header Nunito-Regular">
            {{header_title.title}}
        </div>
        <div class="description Nunito-Regular">
            {{header_title.description}}
        </div>
    </div>
</template>

<script>
    export default {
        props:  ["header_title"]
    }
</script>

<style>
.title{
    margin-left: 38px;
}
.header{
    font-size: 1.5rem;
    line-height: 33px;
    color: #000000;
}
.description{
    font-size: 1.2rem;
    line-height: 25px;
    color: #000000;
}
</style>