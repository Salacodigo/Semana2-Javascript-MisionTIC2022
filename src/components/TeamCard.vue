<template>

    <div class="card text-white bg-dark" id="box-team">
        <div class="d-flex justify-content-center p-2">
            <img :src="member.imagen" alt="fotografia equipo" id="img_team">
        </div>
        <div class="card-body">
            <h5 class="card-title">Team Member: {{member.codigo}}</h5>
            <p class="card-text">{{member.nombre}}</p>
            <p class="card-text">{{member.rol}}</p>
            <p class="card-text">{{member.descripcion}}</p>
        </div>
        <div class="card-footer">
            <small class="text-muted">Last updated 3 mins ago</small>
        </div>
    </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style scoped>
    #img_team{
        width:200px;
        height:200px;
    }

    #box-team{
        width:445px;
        height:550px;
    }
</style>
