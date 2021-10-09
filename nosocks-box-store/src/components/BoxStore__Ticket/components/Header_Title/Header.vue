<template>
    <div class="ticket__block-info__header_title">
        <div class="ticket__block-info__header_title__title Nunito-Bold">
            {{header.title}}
        </div>
        <div class="ticket__block-info__header_title__discription Nunito-Regular">
            {{header.description}}
        </div>
        <div class="ticket__block-info__header_title__star">
            <star
            v-for="i in 5" :key="i"
            v-bind:star="[i, rating]"/>

        </div>
        <div v-if="header.status == 'pre-order'" class="ticket-buy__ticket ticket__pre_order Nunito-Bold">
            предзаказ
        </div>
        <div v-else class="ticket-buy__ticket ticket__new Nunito-Bold">
            новинка
        </div>
    </div>
</template>

<script>
    import Star from "@/components/Star/Star"
    export default {
        props:['header', 'rating'],
        components: {
            "star": Star
        }
    }
</script>

<style>
.ticket__block-info__header_title{
    position: relative;
}
.ticket__block-info__header_title__title{
    font-size: 18px;
    line-height: 25px;
    color: #000000;
}
.ticket__block-info__header_title__discription{
    font-size: 14px;
    line-height: 19px;
    color: #000000;

    margin-top:-3px;
}
.ticket__block-info__header_title__star{
    display: grid;
    grid-template-columns: repeat(5, 16px);
    grid-column-gap: 3px;
    margin-top: 4px;
}
.ticket-buy__ticket{
    position: absolute;
    top: 3px;
    left: 228px;
    height: 20px;
    background: #F91616;
    font-size: 14px;
    line-height: 19px;
    color: #FFFFFF;
    text-align: center;
}
.ticket__new{
    width: 63px;
}
.ticket__pre_order{
    width: 75px;
}
</style>