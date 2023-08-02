<template>
  <center><h1>About</h1></center>
</template>
<script>
  import { onMounted } from 'vue';

  export default{
    setup(props, Context){
      onMounted(() => {
        Context.emit("id-menu", 3);
      } )
    }
  }
</script>