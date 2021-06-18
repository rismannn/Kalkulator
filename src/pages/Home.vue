<template>
    <h1>Aplikasi Kalkulator</h1>
    <table>
        <tr>
            <td><input type="number" v-model="input1"></td>
        </tr>
        <tr>
            <td><input type="number" v-model="input2"></td>
        </tr>
    </table><br/>
    <div>
        <button v-on:click="tambah">+</button>
        <button v-on:click="kurang">-</button>
        <button v-on:click="kali">x</button>
        <button v-on:click="bagi">/</button>
    </div>
    <div>
        <h1>Hasilnya adalah {{ hasil }}</h1>
    </div>
</template>

<script>
export default {
    data(){
        return{
            hasil : 0
        }
    },
        methods:{
            tambah(){
                this.hasil = parseInt(this.input1) + parseInt(this.input2);
            },
            kurang(){
                this.hasil = parseInt(this.input1) - parseInt(this.input2);
            },
            kali(){
                this.hasil = parseInt(this.input1) * parseInt(this.input2);
            },
            bagi(){
                this.hasil = parseInt(this.input1) / parseInt(this.input2);
            },
        }
}
</script>
