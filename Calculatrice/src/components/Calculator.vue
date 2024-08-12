<script setup>
import { ref } from 'vue';
const nombre1 = ref(0);
const nombre2 = ref(0);
const addition = ref(0);
const multiplication = ref(0);
const soustraction = ref(0);
const division = ref(0);

const calculer = () => {
  addition.value = nombre1.value + nombre2.value;
  multiplication.value = nombre1.value * nombre2.value;
  soustraction.value = nombre1.value - nombre2.value;
  division.value = nombre2.value !== 0 ? nombre1.value / nombre2.value : 'Division par zéro';
};
</script>

<template>
  <div>
    <div class="mb-3">
      <label for="nombre1" class="form-label">Nombre 1</label>
      <input type="number" id="nombre1" v-model="nombre1" @input="calculer" class="form-control" />
    </div>
    <div class="mb-3">
      <label for="nombre2" class="form-label">Nombre 2</label>
      <input type="number" id="nombre2" v-model="nombre2" @input="calculer" class="form-control" />
    </div>

    <div>
      <label for="addition">Addition</label>
      <input type="text" id="addition" v-model="addition" readonly class="form-control" />
    </div>
    <div>
      <label for="multiplication">Multiplication</label>
      <input type="text" id="multiplication" v-model="multiplication" readonly class="form-control" />
    </div>
    <div>
      <label for="soustraction">Soustraction</label>
      <input type="text" id="soustraction" v-model="soustraction" readonly class="form-control" />
    </div>
    <div>
      <label for="division">Division</label>
      <input type="text" id="division" v-model="division" readonly class="form-control" />
    </div>
  </div>
</template>

<style scoped>
/* .mb-3 {
  margin-bottom: 1rem;
} */
</style>
