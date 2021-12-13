<template>
  <div class="menu">        
      <a :class="{ active: value }" :href="thumb">{{ option }}</a>
  </div>
</template>

<script>
export default {
    name: 'Menu',
    props:{
        option: String,
        thumb: String,
        value: Boolean,
    }
}
</script>

<style scoped lang="scss">
.menu{
     a{
        text-decoration: none;
        text-transform: uppercase;
        color: white;
        font-size: 14px;
        font-weight: 600;
        margin-left: 20px;
        &.active,
        &:hover{
            color: #1a948f;
        }
    }
}

</style>