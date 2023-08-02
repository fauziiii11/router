<template>
    <center>
    <div v-if="detail == undefined">
        <center><h1>404 NOT FOUND</h1></center>
    </div>
    <div v-else>
        <img :src="gambar(detail.img)" alt="">
    <h1>Detail {{ detail.nama }}</h1>
    <h4>Harga : {{ detail.harga }}</h4>
    <h4>Deskripsi : {{ detail.des }}</h4>
</div>
</center>
  </template>
<script>
import { produk } from '@/assets/Produk';


export default {
    props: [
        "id_produk",
        
        
    ],
    setup(props){
        
        const gambar = (NamaFoto) => {
          return '../src/assets/img/'+ NamaFoto +'';
      }
        const detail = produk["produk"].find(function(item) {
            return item.id == props.id_produk
            
        });
        
        
        return{
            detail,
            gambar
            
            

        }
    }
}
</script>