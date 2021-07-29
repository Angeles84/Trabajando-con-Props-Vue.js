<template>
    <ul>
      <li>
        {{nuevaTarea}} <button type="button" @click="BorrarTarea(index)">Eliminar</button>
      </li>
    </ul>
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
ul {
  width: 30%;
  margin: 0 auto;
  text-align: left;
  padding-left: 16em;
}
</style>
