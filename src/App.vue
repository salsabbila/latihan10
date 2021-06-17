<template>
  <Title title="Catatan pengeluaran"/>
  <FormMahasiswa @entri-mahasiswa = "entriMahasiswa($event)"/>
  <ListMahasiswa v-if="dataMahasiswa.length>0" :dataMahasiswalist="dataMahasiswa"/>
</template>

<script>
import Title from './components/Title.vue'
import FormMahasiswa from './components/FormMahasiswa.vue'
import ListMahasiswa from './components/ListMahasiswa.vue'
export default {
  name: 'App',
  components: {
    Title,
    ListMahasiswa,
    FormMahasiswa,
  },
  data(){
    return{
      dataMahasiswa : [
        {nim : 'D111811131', nama : 'Indah Elviyana', kelas : 'IF 18 B'},
        {nim : 'D111811123', nama : 'Indah', kelas : 'IF 18 B'},
        {nim : 'D111811112', nama : 'Elviyana', kelas : 'IF 18 B'}
      ],
    }
  },
  methods:{
    entriMahasiswa(event){
      this.dataMahasiswa.push(event);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>