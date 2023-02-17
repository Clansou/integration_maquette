<script>
export default {
  props: ['img','name','subname','subimg','activeColor1','activeColor2']
}
</script>

<template>
    <div class="transaction">
        <img :src="img" alt=''>
        <div>
            <p>{{ name }}</p>
            <p>{{ subname }}</p>
        </div>
        <div>
            <p>Market Cap</p>
            <p class="price" :style="{ color: activeColor1}">$40,243.70</p>
        </div>
        <div>
            <p> 24h change</p>
            <p class="change" :style="{ color: activeColor2}">+1,56</p>
        </div>

        <img :src="subimg" alt=''>
        <button>Trade</button>
    </div>

</template>
<style>

.transaction{
    display: flex;
    justify-content: space-around;
    background: rgba(32, 35, 43, 0.7);
    padding: 12px 24px;
    border-radius: 30px;
    font-size: 14px;
    gap: 24px;
}
.transaction>button{
    background: #000000;
    border-radius: 30px;
    padding: 6px 18px;   
    color: #fff; 
}
.transaction>img{
    height: fit-content;
    margin-top: auto;
    margin-bottom: auto;
}
.transaction>div{
    display: flex;
    flex-direction: column;
    justify-content: space-around;
}
.transaction :nth-child(2) :nth-child(2){
    opacity: 0.7;
}
@media (max-width: 800px) {
        .transaction{
            margin-left: auto;
            margin-right: auto;
            width: 85%;
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            grid-template-rows: 1fr 1fr;
        }
    }




</style>