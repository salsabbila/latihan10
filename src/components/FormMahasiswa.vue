<template>
    <form class="form-mahasiswa" @submit.prevent = "tambah">
<div>
    <label>NIM</label>
    <input v-model = "nim" type="text" id = "nim_mhs"/>
</div>
<div>
    <label>Nama</label>
    <input v-model = "nama" type="text" id = "nama_mhs"/>
</div>
<div>
    <label>Kelas</label>
    <input v-model = "kelas" type="text" id = "kelas_mhs"/>
</div>
<div>
<button>Tambah</button>
</div>
    </form>
</template>

<script>
export default({
    data() {
        return {
            nim : null,
            nama : null,
            kelas : null,
        }
    },
    methods:{
        tambah(){
            this.$emit('entri-mahasiswa',{
                nim : this.nim,
                nama : this.nama,
                kelas : this.kelas,
            });
            this.nim = null,
            this.nama = null,
            this.kelas = null,
            document.getElementById("nim_mhs").focus()
        }
    }
})
</script>