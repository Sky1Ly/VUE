<template>
    <div>
        <h1>FormInscripción</h1>

        <form class="w-50" @submit.prevent="formCrearUsuario">
            <div class="mb-3">
                <label for="nombre" class="form-label">Nombre</label>
                <input type="text" name="nombre" id="nombre" class="form-control" v-model="nombre">
            </div>
            <div class="mb-3">
                <label for="apellido" class="form-label">apellido</label>
                <input type="text" name="apellido" id="apellido" class="form-control" v-model="apellido">
            </div>
            <div class="mb-3">
                <label for="email" class="form-label">email</label>
                <input type="text" name="email" id="email" class="form-control" v-model="email">
            </div>
            <div class="mb-3">
                <label for="telefono" class="form-label">telefono</label>
                <input type="text" name="telefono" id="telefono" class="form-control" v-model="telefono">
            </div>
            <div class="d-grid">
                <button type="submit" class="btn btn-outline-primary"></button>
            </div>
        </form>
    </div>
</template>
<script>
export default {
    name: 'FormInscripcion',
    data() {
        return {
            nombre: '',
            apellido: '',
            email: '',
            telefono: '',
        }
    },
    methods: {
        formCrearUsuario(){
            console.log(this.nombre, this.apellido, this.email, this.telefono)
        }
    }
}
</script>
<style></style>