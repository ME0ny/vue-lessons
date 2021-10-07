<template>
    <div class="item">
        <div class="ticket">
            <img src="./img/ticket_main_img.png" class="ticket__main-img" alt="">
            <div class="ticket__block-info">
                <div class="ticket__block-info__header_title">
                    <div class="ticket__block-info__header_title__title Nunito-Bold">
                        {{ ticket.title}}
                    </div>
                    <div class="ticket__block-info__header_title__discription Nunito-Regular">
                        {{ ticket.description}}
                    </div>
                    <div class="ticket__block-info__header_title__star">
                        <div class="star star-fire"></div>
                        <div class="star star-fire"></div>
                        <div class="star star-fire"></div>
                        <div class="star star-fire"></div>
                        <div class="star star-fireless"></div>
                    </div>
                    <div class="ticket-buy__new Nunito-Bold">
                        новинка
                    </div>
                </div>
                <div class="ticket__size">
                    <div class="ticket__size-title Nunito-Bold">
                        Размер
                    </div>
                    <div class="ticket__size-wrapper Nunito-Regular">
                        <div class="ticket__size-item ticket__size-item-deactivate">
                            <span>36</span>
                        </div>
                        <div class="ticket__size-item ticket__size-item-deactivate">
                            <span>36</span>
                        </div>
                        <div class="ticket__size-item ticket__size-item-deactivate">
                            <span>36</span>
                        </div>
                        <div class="ticket__size-item ticket__size-item-deactivate">
                            <span>36</span>
                        </div>
                        <div class="ticket__size-item ticket__size-item-activate">
                            <span>36</span>
                        </div>
                    </div>
                </div>
                <div class="ticket__socks_into">
                    <div class="ticket__socks_into-title Nunito-Bold">
                        Носки в наборе
                    </div>
                    <div class="ticket__socks_into-wrapper">
                        <div class="ticket__socks_into-item">
                            <img v-bind:src="ticket.socks[0]"/>
                        </div>
                        <div class="ticket__socks_into-item">
                            <img v-bind:src=ticket.socks[1]>
                        </div>
                        <div class="ticket__socks_into-item">
                            <img v-bind:src=ticket.socks[2]>
                        </div>
                    </div>
                </div>
                <div class="ticket-buy__footer">
                    <div class="ticket-buy__footer__number">
                        <div class="ticket-buy__footer__number-title Nunito-Bold">
                            Осталось
                        </div>
                        <div class="ticket-buy__footer__number-item Nunito-Regular">
                            {{ticket.status.value}} наборов
                        </div>
                    </div>
                    <button class="ticket-buy__footer__buy">
                        {{ticket.price}} руб
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props:['ticket'],
    }
</script>

<style>
.item {
  height: 544px;
  width: 322px;
}
.ticket {
    width: 322px;
    height: 544px;
    background: #FFFFFF;
    box-shadow: 4px 4px 10px rgba(0, 0, 0, 0.1);
    border-radius: 20px;
}
.ticket__main-img{
    width: 100%;
}
.ticket__block-info{
    margin-top: 28px;
    margin-left: 19px;
}
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
.star{
    width: 16px;
    height: 16px;
}
.star-fire{
    background: url("./img/star-fire.png");
}
.star-fireless{
    background: url("./img/star-fireless.png");
}
.ticket-buy__new{
    position: absolute;
    top: 3px;
    left: 228px;
    width: 63px;
    height: 20px;
    background: #F91616;
    font-size: 14px;
    line-height: 19px;
    color: #FFFFFF;
    text-align: center;
}
.ticket__size{
    margin-top: 15px;
    font-size: 14px;
    line-height: 19px;
    color: #000000;
}
.ticket__size-title{
    margin-top: 2px;
}
.ticket__size-wrapper{
    display: inline-flex;
    flex-wrap: wrap;
    gap: 4px;
    margin-top: 5px;
}
.ticket__size-item{
    position: relative;
    font-size: 12px;
    line-height: 16px;
    color: #000000;
    text-align: center;
    width: 20px;
    height: 20px;
    line-height: 100%;
    border-radius: 50%;
}
.ticket__size-item-activate{
    background-color: #F91616;
}
.ticket__size-item-activate > span{
    display: inline-block;
    vertical-align: middle;
    color: white;
    margin-top: 4px;
}
.ticket__size-item-deactivate{
    background-color: #fff;
}
.ticket__size-item-deactivate > span{
    display: inline-block;
    vertical-align: middle;
    color: black;
    margin-top: 4px;
}
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
    margin-top: 4px;
}
.ticket-buy__footer{
    position: relative;
    margin-top: 45px;
}
.ticket-buy__footer__number{
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
}
</style>