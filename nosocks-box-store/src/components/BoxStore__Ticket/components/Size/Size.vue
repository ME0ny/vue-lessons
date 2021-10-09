<template>
    <div class="ticket__size">
        <div class="ticket__size-title Nunito-Bold">
            Размер
        </div>
        <div class="ticket__size-wrapper Nunito-Regular">
            <div v-for="i in size" :key="i" class="ticket__size-item ticket__size-item-deactivate">
                <span>{{i}}</span>
            </div>
        </div>
    </div>
</template> 

<script>
    export default {
        props:['size'],
    }
</script>

<style>
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
</style>