<template>
    <h1>404 Not Found</h1>
</template>


<script>
  import { onMounted } from 'vue';

  export default{
    setup(props, Context){
      onMounted(() => {
        Context.emit("id-menu", 6);
      } )
    }
  }
</script>