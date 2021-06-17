<template>
    <table border="1" class = "center">
        <tr>
            <th>NIM</th>
            <th>Nama Lengkap</th>
            <th>Kelas</th>
        </tr>

        <tr v-for="(mahasiswa, index) in dataMahasiswalist" :key="index">
            <td>{{ mahasiswa.nim }}</td>
            <td>{{ mahasiswa.nama }}</td>
            <td>{{ mahasiswa.kelas }}</td>
        </tr>
    </table>
</template>

<script>
export default {
    props: {
        dataMahasiswalist: Array,
    },
};
</script>
<style scoped>
.center {
    margin-left: auto;
    margin-right: auto;
}
</style>