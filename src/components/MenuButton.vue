<script>
export default {
  props: ['img','text']
}
</script>

<template>
  <div class="MenuButton">
    <img :src="img" alt=''>
    <a>{{ text }}</a>
  </div>
</template>

<style scoped>
    .MenuButton{
        display: grid;
        grid-template-columns: 2fr 4fr;
        align-items: center;
        padding: 9px 15px;
        gap: 16px;
        font-size: 25px;
        font-weight: 500;
        line-height: 38px;
        letter-spacing: 0em;

        
    }
    img{
        height: 38px;
        margin-left: auto;
        margin-right: auto;
    }
</style>