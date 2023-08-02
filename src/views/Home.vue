<template>
  <center><h1>Home</h1></center>
</template>
<script>
  import { onMounted } from 'vue';

  export default{
    setup(props, Context){
      onMounted(() => {
        Context.emit("id-menu", 1);
      } )
    }
  }
</script>