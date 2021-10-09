<template>
    <div class="ticket-buy__footer">
        <div v-if="status == 'pre-order'">
            <div class="ticket-pre_order__footer__number-wrapper">
                <div class="ticket-buy__footer__number-title Nunito-Bold">
                    До выпуска
                </div>
                <div class="ticket-buy__footer__number-item Nunito-Regular">
                    {{value.left.box}} {{value.left.order_name}}
                </div>
            </div>
            <div class="ticket-pre_order__footer__number-time Nunito-Regular">
                Сбор заканчивается через {{value.days.day}} {{value.days.day_name}}
            </div>
            <button class="button ticket-buy__footer__button_buy Nunito-Bold button-up">
                {{price}} руб
            </button>
        </div>
        <div v-else>
            <div class="ticket-pre_order__footer__number-wrapper">
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
    margin-top: 25px;
}
.ticket-pre_order__footer__number-wrapper{
    display: flex;
}
.ticket-buy__footer__number-title{
    font-size: 14px;
    line-height: 19px;
    color: #000000;

}
.ticket-buy__footer__number-item{
    font-size: 12px;
    line-height: 16px;
    color: #000000;
    margin-top: auto;
    margin-left: 11px;
    /* margin-left: 11px; */
}
.ticket-pre_order__footer__number-time{
    font-size: 9px;
    line-height: 12px;
    color: #C4C4C4;
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
    color: #FFFFFF;
    margin-left: 216px;
    margin-top: -33px;
}
.ticket-buy__footer__button_buy:hover{
    box-shadow: 0px 4px 4px rgba(249, 103, 22, 0.25), 0px -4px 4px rgba(249, 103, 22, 0.25), 4px 0px 4px rgba(249, 103, 22, 0.25);
}
.button-up{
    margin-top: -45px;
}
</style>