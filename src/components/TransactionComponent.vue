<script>
export default {
  props: ['img','name','subname','subimg']
}
</script>

<template>
    <div>
        <img :src="img" alt=''>
        <div>
            <p>{{ name }}</p>
            <p>{{ subname }}</p>
        </div>
        <div>
            <p>Market Cap</p>
            <p class="price">$40,243.70</p>
        </div>
        <div>
            <p> 24h change</p>
            <p class="change">+1,56</p>
        </div>

        <img :src="subimg" alt=''>
        <button>Trade</button>
    </div>

</template>