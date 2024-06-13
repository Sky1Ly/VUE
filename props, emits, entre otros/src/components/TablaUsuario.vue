<template>
    <div>
        <h1>TablaUsuario</h1>
        <table class="table">
            <thead>
                <tr>
                    <th scope="col">ID</th>
                    <th scope="col">Nombre</th>
                    <th scope="col">Apellido</th>
                    <th scope="col">Email</th>
                    <th scope="col">Telefono</th>
                    <th scope="col">Acciones</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="usuario in usuarios" :key="usuario.id">
                    <th scope="row">{{ usuario.id }}</th>
                    <th>{{ usuario.nombre }}</th>
                    <th>{{ usuario.apellido }}</th>
                    <th>{{ usuario.email }}</th>
                    <th>{{ usuario.telefono }}</th>
                    <th>Acciones</th>
                </tr>
            </tbody>
        </table>
    </div>
</template>
<script>
export default {
    name: 'TablaUsuario',
    props: {
        usuarios: Array
    }
}
</script>
<style>
    export default {
        name: 'TablaUsuario',
    }
</style>