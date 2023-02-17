<script>
export default {
  props: ['color','img','name','quantity','subname','background']
}
</script>
<template>
    <div class="asset" :style="{ background: background , color: color }">
        <img :src="img" alt="">
        <p>{{ name }}</p>
        <div>
            <p>{{ quantity }}</p>
            <p>{{ subname }}</p>
        </div>
    </div>
</template>
<style scoped>
    .asset{
        padding: 12px 20px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        border-radius: 30px;
    }
    .asset>p{
        margin-left: 8px;
    }
    img{
        width: 20%;
    }
    .asset>div{
        display: flex;
        justify-content: space-between;
        padding: 0 12px;
    }

</style>