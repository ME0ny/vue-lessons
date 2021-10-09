<template>
    <div class="item">
        <div class="ticket">
            <img src="./img/ticket_main_img.png" class="ticket__main-img" alt="">
            <div class="ticket__block-info">
                <ticket-header
                 v-bind:header="{
                     title: ticket.title, 
                     description: ticket.description, 
                     status: ticket.status.status}"
                 v-bind:rating="ticket.rating"/>
                <size-template 
                v-bind:size="ticket.size"
                />
                <socks-template
                v-bind:socks="ticket.socks"
                />
                <ticket-footer 
                v-bind:status="ticket.status.status"
                v-bind:value="ticket.status.value"
                v-bind:price="ticket.price"/>
            </div>
        </div>
    </div>
</template>

<script>
    import Header from "./components/Header_Title/Header"
    import Size from "./components/Size/Size"
    import Socks from "./components/Socks/Socks"
    import Footer from "./components/Footer/Footer"
    export default {
        props:['ticket'],
        components: {
            "ticket-header": Header,
            "size-template": Size,
            "socks-template": Socks,
            "ticket-footer": Footer
        }
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
</style>