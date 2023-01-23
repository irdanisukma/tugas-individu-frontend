<template>
  <!----tempat ngoding html-->
    <div class="bg-slate-500 font-extrabold"> Data Sensor = {{ datasensor }} 
      <button class="bg-orange-500 p-2 rounded-xl" @click="updata">Ambil data Sensor</button>
    </div>
    
  
</template>
<script>


export default{
  data(){
    return{
      datasensor: "Belum ada data",

    }
  },
  created(){
    this.sambutan(),
    this.isi()
  },
  methods:{
    sambutan(){
      alert("Selamat Datang");
    },
    isi(){
      alert("Tugas Individu");
    },
    async updata(){
      const data = await fetch("http://127.0.0.1:3000/ambil")
      const datanya = await data.json()
      this.datasensor = datanya.sensor3
    }
  }
}
//tempat ngoding javascript
</script>

<style>

</style>

