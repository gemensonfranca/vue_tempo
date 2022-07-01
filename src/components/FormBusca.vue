<template>
    <center>
    <form action="">
        <input type="text" class="form_tempo" name="buscar_cidade" placeholder="Busque uma cidade">
    </form>
    </center>
</template>

<style>
    .form_tempo{
        width: 94%;
        margin: 40px 0px;
        height: 40px;
        border-radius: 100px;
        border: solid 1px #cdcdcd;
        padding-left: 20px;
        font-size: 15px;
    }
</style>

<script>
    export default {
        name: 'FormBusca',
        data(){
            return{
                cidadeBusca: "",
            }
        }
    }
</script>