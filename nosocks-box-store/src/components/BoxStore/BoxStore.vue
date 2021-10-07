<template>
    <div class="grid">
        <boxstore-ticket
            v-for="ticket in tickets" :key="ticket"
            v-bind:ticket="ticket"/>
    </div>
</template>

<script>
import Ticket from "@/components/BoxStore__Ticket/Ticket"
export default {
    props:['tickets'],
    components: {
            "boxstore-ticket": Ticket,
    }
}
</script>

<style>
.grid {
  display: grid;
  grid-template-columns: repeat(3, 322px);
  justify-content: space-evenly;;
  grid-row-gap: 5px;
  grid-column-gap: 5px;
  position: relative;
  margin-top: 30px;
  margin-left: 46px;
}

@media screen and (max-width: 1134px) and (min-width: 530px)
{
    .grid {
        grid-template-columns: repeat(2, 241px);
    }
}

@media screen and (max-width: 530px)
{
    .grid {
        grid-template-columns: repeat(1, 241px);
    }
}
</style>
  