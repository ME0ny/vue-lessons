<template>
    <div class="ticket-buy__footer">
        <div v-if="status == 'pre-order'" class="ticket-pre_order__footer__number">
            <div class="ticket-pre_order__footer__number-wrapper">
                <div class="ticket-buy__footer__number-title Nunito-Bold">
                    До выпуска
                </div>
                <div class="ticket-buy__footer__number-item Nunito-Regular">
                    {{value.left.box}} {{value.left.order_name}}
                </div>
            </div>
            <div class="ticket-pre_order__footer__number-time">
                Сбор заканчивается через {{value.days.day}} {{value.days.day_name}}
            </div>
        </div>
        <div v-else class="ticket-buy__footer__number">
            <div class="ticket-buy__footer__number-title Nunito-Bold">
                Осталось
            </div>
            <div class="ticket-buy__footer__number-item Nunito-Regular">
                {{value.left.box}} {{value.left.order_name}}
            </div>
        </div>
        <button class="button ticket-buy__footer__button_buy Nunito-Bold">
            {{price}} руб
        </button>
    </div>
</template>

<script>
    export default {
        props:['status', 'value', 'price'],
    }
</script>

<style>
.ticket-buy__footer{
    position: relative;
    margin-top: 35px;
}
.ticket-pre_order__footer__number-wrapper{
    display: flex;
}
.ticket-buy__footer__number{
    display: flex;
}
.ticket-buy__footer__number-title{
    font-size: 14px;
    line-height: 19px;
    width: 100%;
    color: #000000;
}
.ticket-buy__footer__number-item{
    width: 100%;
    height: 100%;
    font-size: 12px;
    line-height: 16px;
    color: #000000;
    margin-top: auto;
    margin-left: 11px;
}
.ticket-buy__footer__button_buy{
    position: absolute;
    background: #F91616;
    border-radius: 5px;
    background-color: #F91616;
    width: 106px;
    height: 33px;
    border: none;
    outline:none;
    font-size: 14px;
    line-height: 19px;
    color: #FFFFFF;
    margin-left: 216px;
    margin-top: -33px;
}
.ticket-buy__footer__button_buy:hover{
    box-shadow: 0px 4px 4px rgba(249, 103, 22, 0.25), 0px -4px 4px rgba(249, 103, 22, 0.25), 4px 0px 4px rgba(249, 103, 22, 0.25);
}
</style>