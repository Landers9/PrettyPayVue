<template>
  <div class="register">
    <FormRegister/>
  </div>
</template>

<script>
// @ is an alias to /src
import FormRegister from '@/components/FormRegister.vue'

export default {
  name: 'Register',
  components: {
    FormRegister
  }
}
</script>
