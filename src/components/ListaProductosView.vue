<template>
  <div>
    <h1>Productos</h1>
    <p class="text-2xl text-blue-500">{{mensaje}}</p>
    <div v-for="user in users" :key="user.email">
      <p>Nombre: {{ user.name }}</p>
      <p>Email: {{ user.email }}</p>
      <p>Edad: {{ user.age }}</p>
      <br/>
    </div>
  </div>
</template>

<script>

export  default {
  name: 'ProductosView',
  props:{
      mensaje: String,
    users:{
        type:Array,
      required: true
    }
  }
}
</script>