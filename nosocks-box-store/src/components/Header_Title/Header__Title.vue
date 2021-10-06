<template>
    <div class="title">
        <div class="header">
            {{header_title.title}}
        </div>
        <div class="description">
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
@font-face {
    font-family: "Nunito";
    src: local("Nunito"),
    url(./fonts/Nunito-Regular.ttf) format("truetype");
}
.title{
    margin-left: 38px;
}
.header{
    font-family: Nunito;
    font-style: normal;
    font-weight: normal;
    font-size: 24px;
    line-height: 33px;
    color: #000000;
}
.description{
    font-family: Nunito;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 25px;
    color: #000000;
}
</style>