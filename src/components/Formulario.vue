<script setup>
import { reactive } from 'vue';

const paciente = reactive({
  nombre:'',
  propietario:'',
  email: '',
  alta:'',
  sintomas: ''
})
const validar = e =>{
  e.preventDefault()
  console.log("validadno")
}
</script>
 
<template>
  <div class="md:w-1/2">
    <h2 class="font-black text-3xl text-center">Seguimiento paciente</h2>
    <p class="text-lg mt-5 text-center mb-10">
      Añade Pacientes y
      <span class="text-indigo-600 font-bold">Adminístralos </span>
    </p>
    <form @submit="validar" class="bg-white shadow-md rounded-lg py-10 px-5 mb-10">
      <div class="mb-5">
        <label for="mascota" class="block text-gray-700 uppercase font-bold">
          Nombre mascota
        </label>
        <input
          type="text"
          id="mascota"
          placeholder="NOMBRE DE LA MASCOTA"
          class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md"
          v-model="paciente.nombre"
        />
      </div>
      <div class="mb-5">
        <label for="mascota" class="block text-gray-700 uppercase font-bold">
          Nombre propietario
        </label>
        <input
          type="text"
          id="propietario"
          placeholder="NOMBRE DE LA MASCOTA"
          class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md"
          v-model="paciente.propietario"
        />
      </div>
      <div class="mb-5">
        <label for="mascota" class="block text-gray-700 uppercase font-bold">
          Email
        </label>
        <input
          type="email"
          id="email"
          placeholder="EMAIL"
          class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md"
          v-model="paciente.email"
        />
      </div>
      <div class="mb-5">
        <label for="mascota" class="block text-gray-700 uppercase font-bold">
          Alta
        </label>
        <input
          type="date"
          id="alta"
          class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md"
          v-model="paciente.alta"
        />
      </div>
      <div class="mb-5">
        <label for="mascota" class="block text-gray-700 uppercase font-bold">
          Registrar sintomas
        </label>
        <textarea
          id="sintomas"
          placeholder="DESCRIBE SINTOMAS"
          class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md h-40"
          v-model="paciente.sintomas"
        ></textarea>
      </div>
      <input
        type="submit"
        class="bg-indigo-600 w-full p-3 text-white uppercase font-bold hover:bg-indigo-700 cursor-pointer transition-colors"
        value="Registrar paciente"
      />
    </form>
  </div>
</template>
