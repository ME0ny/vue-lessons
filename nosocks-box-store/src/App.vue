<template>
  <div id="App">
    <header-template />
    <box-store 
    v-bind:tickets="tickets"/>
    <div class="menu">
      <btn-main />
      <btn-collections />
    </div>
  </div>
</template>

<script>
import Header from "@/components/Header/Header"
import BoxStore from "@/components/BoxStore/BoxStore"
export default {
  name: 'App',
  data() {
    return {
      tickets: [
        {
          title: "Дальневосточные носки",
          description: "Достопримечательности региона",
          rating: 4,
          size: [36, 37, 38, 39, 40, 41],
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/icra.png"),
          ],
          status:{
            status: "buy",
            value: {
              left: {
                box: "100",
                order_name: "наборов"
              },
            }
          },
          price: 450
        },
        {
          title: "Дальневосточные носки",
          description: "Достопримечательности региона",
          rating: 5,
          size: [36, 37, 38, 39, 40, 41],
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/mamont.png"),
            require("@/img/rocket.png")
          ],
          status:{
            status: "buy",
            value: {
              left: {
                box: "1",
                order_name: "набор"
              },
            }
          },
          price: 450
        },
        {
          title: "Дальневосточные носки",
          description: "Достопримечательности региона",
          rating: 0,
          size: [36, 37, 38, 39, 40, 41],
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/icra.png"),
            require("@/img/mamont.png"),
            require("@/img/rocket.png")
          ],
          status:{
            status: "pre-order",
            value: {
              left: {
                box: "100",
                order_name: "заказов"
              },
              days:{
                day: 15,
                day_name: "дней"
              }
            }
          },
          price: 4400
        },
        {
          title: "Дальневосточные носки",
          description: "Достопримечательности региона",
          rating: 4,
          size: [36, 37, 38, 39, 40, 41],
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/icra.png"),
          ],
          status:{
            status: "buy",
            value: {
              left: {
                box: "100",
                order_name: "наборов"
              },
            }
          },
          price: 450
        },
        {
          title: "Дальневосточные носки",
          description: "Достопримечательности региона",
          rating: 5,
          size: [36, 37, 38, 39, 40, 41],
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/mamont.png"),
            require("@/img/rocket.png")
          ],
          status:{
            status: "buy",
            value: {
              left: {
                box: "1",
                order_name: "набор"
              },
            }
          },
          price: 450
        },
        {
          title: "Дальневосточные носки",
          description: "Достопримечательности региона",
          rating: 0,
          size: [36, 37, 38, 39, 40, 41],
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/icra.png"),
            require("@/img/mamont.png"),
            require("@/img/rocket.png")
          ],
          status:{
            status: "pre-order",
            value: {
              left: {
                box: "100",
                order_name: "заказов"
              },
              days:{
                day: 15,
                day_name: "дней"
              }
            }
          },
          price: 4400
        },
        {
          title: "Дальневосточные носки",
          description: "Достопримечательности региона",
          rating: 4,
          size: [36, 37, 38, 39, 40, 41],
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/icra.png"),
          ],
          status:{
            status: "buy",
            value: {
              left: {
                box: "100",
                order_name: "наборов"
              },
            }
          },
          price: 450
        },
        {
          title: "Дальневосточные носки",
          description: "Достопримечательности региона",
          rating: 5,
          size: [36, 37, 38, 39, 40, 41],
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/mamont.png"),
            require("@/img/rocket.png")
          ],
          status:{
            status: "buy",
            value: {
              left: {
                box: "1",
                order_name: "набор"
              },
            }
          },
          price: 450
        },
        {
          title: "Дальневосточные носки",
          description: "Достопримечательности региона",
          rating: 0,
          size: [36, 37, 38, 39, 40, 41],
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/icra.png"),
            require("@/img/mamont.png"),
            require("@/img/rocket.png")
          ],
          status:{
            status: "pre-order",
            value: {
              left: {
                box: "100",
                order_name: "заказов"
              },
              days:{
                day: 15,
                day_name: "дней"
              }
            }
          },
          price: 4400
        },
        {
          title: "Дальневосточные носки",
          description: "Достопримечательности региона",
          rating: 4,
          size: [36, 37, 38, 39, 40, 41],
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/icra.png"),
          ],
          status:{
            status: "buy",
            value: {
              left: {
                box: "100",
                order_name: "наборов"
              },
            }
          },
          price: 450
        },
        {
          title: "Дальневосточные носки",
          description: "Достопримечательности региона",
          rating: 5,
          size: [36, 37, 38, 39, 40, 41],
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/mamont.png"),
            require("@/img/rocket.png")
          ],
          status:{
            status: "buy",
            value: {
              left: {
                box: "1",
                order_name: "набор"
              },
            }
          },
          price: 450
        },
        {
          title: "Дальневосточные носки",
          description: "Достопримечательности региона",
          rating: 0,
          size: [36, 37, 38, 39, 40, 41],
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/icra.png"),
            require("@/img/mamont.png"),
            require("@/img/rocket.png")
          ],
          status:{
            status: "pre-order",
            value: {
              left: {
                box: "100",
                order_name: "заказов"
              },
              days:{
                day: 15,
                day_name: "дней"
              }
            }
          },
          price: 4400
        },
      ]
    }
  },
  components: {
    "header-template": Header,
    "box-store": BoxStore
  }
}
</script>

<style>
@font-face {
font-family: "Nunito-Regular";
src: url(./fonts/Nunito-Regular.ttf) format("truetype");
}
@font-face {
font-family: "Nunito-Bold";
src: url(./fonts/Nunito-Regular.ttf) format("truetype");
}
#app {
  margin-top: 23px;
}
.Nunito-Regular{
  font-family: "Nunito-Regular";
  font-style: normal;
  font-weight: normal;
}
.Nunito-Bold{
  font-family: "Nunito-Bold";
  font-style: normal;
  font-weight: bold;
}
</style>
