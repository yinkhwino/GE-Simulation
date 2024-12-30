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
  <input v-model="msg" type="number" placeholder="type msg"></input><br>
  <label>Product A1: </label><br>
  <input v-model="msg1" type="number" placeholder="type msg1"></input><br>
  <button class="btn btn-primary" v-if="editing" @click="doEdit(false)">Compute</button>
  <button v-else @click="doEdit(true)">Compute</button>
</form>
<!--Add your own Compute function of Vite-->
</template>
