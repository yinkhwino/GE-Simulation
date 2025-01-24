<script setup>
import { ref, computed} from 'vue'
const heading = ref('Compute Product!')
const msg = ref(0)
const msg1 = ref(1100)
const editing = ref(false)
const doEdit = (e)=>{editing.value = e}
</script>

<template>
<div class = "heading">
  <img src="https://upload.wikimedia.org/wikipedia/commons/2/2e/GE_Aerospace_logo.svg"></img>
  <h1>{{ heading }}</h1>
</div>
<form class="submit class" v-if="!editing">
  <label>Product A: </label><br>
  <input v-model="productA" type="number" placeholder="type number"></input><br>
  <label>Product A1: </label><br>
  <input v-model="productA1" type="number" placeholder="type number"></input><br>
  <button class="btn btn-primary" v-if="editing" @click="doEdit(false)">Compute</button>
  <button v-else @click="doEdit(true)">Compute</button>
</form>
<p v-if="editing" class="computed-result">Computed product: {{ computedProduct }}</p>
</template>

<script setup>
import { ref, computed } from 'vue'
import { compute } from './Utils/Function.js'

const heading = ref('Compute Product!')
const productA = ref(0)
const productA1 = ref(0)
const editing = ref(false)

const toggleEdit = () => {
  editing.value = !editing.value
}

const computedProduct = computed(() => {
  return compute(productA.value, productA1.value)
})
</script>
