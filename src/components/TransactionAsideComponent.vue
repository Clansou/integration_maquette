<script>
export default {
  props: ['img','name','state','price','date','activeColor1']
}
</script>

<template>
    <div class="transactionasidediv">
        <img :src="img" alt="">
        <div>
            <p >{{ name }}</p>
            <p>{{ state }}</p>
        </div>
        <div>
            <p :style="{ color: activeColor1}">{{ price }}</p>
            <p>{{ date }}</p>
        </div>
    </div>
</template>

<style scoped>
    .transactionasidediv{
        display: grid;
        grid-template-columns: 2fr 3fr 5fr;
        align-items: center;
        padding: 8px;
        gap: 16px;
        font-size: 19px;

    }
    img{
        height: fit-content;
    }
    .transactionasidediv>div{
        flex-direction: column;
    }
    .transactionasidediv div :nth-child(2){
        opacity: 0.7;
    }
    @media (max-width: 400px) {
        .transactionasidediv{
            grid-template-columns: 2fr 2fr;
        }
        .transactionasidediv div:nth-child(2){
            display: none;
        }
    }
    
    
</style>