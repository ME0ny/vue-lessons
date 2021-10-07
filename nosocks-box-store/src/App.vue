<template>
  <div id="App">
    <header-template />
    <box-store 
    v-bind:tickets="tickets"/>
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
          rating: 1,
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/icra.png"),
            require("@/img/mamont.png"),
            require("@/img/rocket.png")
          ],
          status:{
            status: "but",
            value: 200
          },
          price: 450
        },
        {
          title: "Дальневосточные носки 2",
          description: "Достопримечательности региона 2",
          rating: 4,
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/icra.png"),
            require("@/img/mamont.png"),
            require("@/img/rocket.png")
          ],
          status:{
            status: "but",
            value: 100
          },
          price: 4500
        },
        {
          title: "Дальневосточные носки 3",
          description: "Достопримечательности региона 3",
          rating: 4,
          socks: [
            require("@/img/petrogl.png"),
            require("@/img/icra.png"),
            require("@/img/mamont.png"),
            require("@/img/rocket.png")
          ],
          status:{
            status: "but",
            value: 102
          },
          price: 4504
        }
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
