<template>
    <div>
        <div v-if="star[1] - star[0] >= 0" class="star star-fire"></div>
        <div v-else class="star star-fireless"></div>
    </div>
</template>

<script>
    export default {
        props:['star'],
    }
</script>

<style>
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
</style>