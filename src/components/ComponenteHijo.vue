<template>
  <li>
    {{nuevaTarea}} <button type="button" @click="BorrarTarea(index)">Eliminar</button>
  </li>
</template>

<script>

 export default {
    name: 'ComponenteHijo',
    props: {
      nuevaTarea: {
        type: String
      }
    },
    methods: {
      BorrarTarea(index) {
        this.$emit("borrarTarea", index);
      }
    }
  };
</script>

<style scoped>
button {
  background-color: #d6e2f5;
  border: 1.7px solid #4b4b4b;
  margin-left: 2px;
  cursor: pointer;
  padding: 3.5px 5px;
}

</style>
