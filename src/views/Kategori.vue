<template>
<center><h1>kategori</h1>
  <div class="flex-container">
      <div v-for="kategori in cek" :key="kategori.id" class="card">
        <img class="img" :src="img(kategori.img)" alt="Category image" />
      <router-link class="container" :to="{ name : 'DetailKategori', params:{id_kategori : kategori.id}}">
          <h4>{{ kategori.namakategori }}</h4>
          
      </router-link>
  </div>
  </div>
</center>
</template>
<script>
import { onMounted, reactive } from 'vue';
import { kategori } from '@/assets/Kategori';

export default{
  setup(props,context){

      const cek = reactive(kategori["kategori"]);
      
        const img = (NamaFoto) => {
          return '../src/assets/img/'+ NamaFoto +'';
      }

      onMounted(() => {
          context.emit("id-menu",5)
      });

      return{
          cek,
          img
      }
  }
}
</script>
<style scoped>

.card {
  box-shadow: 0 4px 8px 0 rgba(0,0, 0, 0.2);
  transition: 0.3s;
  margin: 10px;
  min-width: 200px;
  cursor: pointer;
}
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0, 0, 0.2);
}
.container {
  padding: 2px 16px;
}
.img{
  width: 150px;
}
</style>