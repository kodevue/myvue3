<script setup>
import { ref } from 'vue'

let myform = ref()
let isFormSubmited = ref(false)

let saveForm = () => {
  isFormSubmited.value = true

  // console.log(myform.value)
  if (!myform.value.checkValidity()) {
    alert('Invalid')
    return
  }

  alert('Valid')
}
</script>


<template>
  <h1 class="alert alert-secondary">Basic Validation</h1>

  <form
    class="needs-validation"
    :class="{ 'was-validated': isFormSubmited }"
    novalidate
    ref="myform"
  >
    <input
      type="text"
      placeholder="Enter username"
      class="form-control form-control-lg mt-1"
      required
      minlength="3"
    />
    <input
      type="email"
      placeholder="Enter email"
      class="form-control form-control-lg mt-1"
      required
      minlength="3"
    />

    <input type="button" value="Submit" class="btn btn-secondary w-100 mt-2" @click="saveForm" />
  </form>
</template>