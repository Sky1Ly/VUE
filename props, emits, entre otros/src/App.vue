<script>
import TablaUsuario from './components/TablaUsuario.vue'

export default {
  name: 'App',
  components: {
    TablaUsuario,
  },
  data() {
    return {
      usuariosAPI: []
    }
  },
  methods: {
    async getUsuarios() {
      try {
        const response = await fetch('./data.json')
        const data = await response.json()

        this.usuariosAPI = data.usuarios

      } catch (err) {
        console.error(err);
      }
    },
  },

  async mounted() {
    await this.getUsuarios()
  },
}
</script>

<template>
  <div>
    <h1>Home</h1>

    <TablaUsuario :usuarios="usuariosAPI"/>
  </div>
</template>

<style scoped></style>
