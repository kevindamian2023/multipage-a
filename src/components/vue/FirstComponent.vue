<script setup>
import { ref } from "vue";

let number = ref(5)

function add() {
  number.value++
  console.log(number.value)
}
function add2() {
  if (number.value > 0) {
    number.value--
  }
}
</script>

<template>
  <div class="max-w-96 bg-blue-200 rounded py-3 px-5 mx-auto">
    <div class="ml-6 bg-red-400 size-8 flex items-center justify-center rounded-full" v-if="number > 0">
      {{ number }}
    </div>
    <div v-else>
      Nadie te escribe :/
    </div>
    <div class="flex space-x-5">
      <div class="bg-blue-400 size-8 flex items-center justify-center rounded-full" @click="add2()">
        -
      </div>
      <div class="bg-blue-400 size-8 flex items-center justify-center rounded-full" @click="add()">
        +
      </div>
    </div>
  </div>
</template>
