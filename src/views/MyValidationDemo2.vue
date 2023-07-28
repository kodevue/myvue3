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
  <div class="row justify-content-center">
    <div class="col-12 col-md-6">
      <h1 class="alert alert-secondary">Basic Validation</h1>
      <form
        class="needs-validation"
        :class="{ 'was-validated': isFormSubmited }"
        novalidate
        ref="myform"
      >
        <div>
          <input
            type="text"
            placeholder="Enter username"
            class="form-control form-control-lg mt-1"
            required
            minlength="3"
          />
          <div class="valid-feedback">Looks good!</div>
          <div class="invalid-feedback">Please choose a username.</div>
        </div>

        <div>
          <input
            type="email"
            placeholder="Enter email"
            class="form-control form-control-lg mt-1"
            required
            minlength="3"
          />
          <div class="valid-feedback">Looks good!</div>
          <div class="invalid-feedback">Please choose a Email.</div>
        </div>

        <input
          type="button"
          value="Submit"
          class="btn btn-secondary w-100 mt-2"
          @click="saveForm"
        />
      </form>
    </div>
  </div>
</template>