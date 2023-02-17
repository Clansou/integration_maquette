<script>
export default {
  props: ['img','name','quantity','subname','background']
}
</script>
<template>
    <div>
        <img :src="img" alt="">
        <p>{{ name }}</p>
        <div>
            <p>{{ quantity }}</p>
            <p>{{ subname }}</p>
        </div>
    </div>
</template>